<h1 align="center">🔥 Forest Fire Impact & Recovery Analysis</h1>

<p align="center">
  Remote Sensing-based assessment of biomass loss, carbon emissions, and vegetation recovery dynamics
</p>

<hr>

<h2>📌 Overview</h2>
<p>
This study integrates satellite data and statistical modeling to quantify the impact of forest fires on 
biomass, carbon emissions, and ecosystem recovery. Using MODIS and Landsat datasets, the workflow 
captures pre-fire, during-fire, and post-fire dynamics with a focus on NDVI, evapotranspiration (ET), 
and carbon flux.
</p>

<hr>

<h2>🛰️ Data Sources</h2>
<ul>
  <li>MODIS Vegetation Continuous Fields (MOD44B)</li>
  <li>MODIS NDVI Time Series</li>
  <li>Landsat 8 Surface Reflectance</li>
  <li>ERA5-Land Climate Data</li>
</ul>

<hr>

<h2>⚙️ Methodology</h2>

<h3>1. Biomass Estimation</h3>
<p>
Above-Ground Biomass (AGB) was derived using MODIS tree cover:
</p>
<pre>
AGB = Tree Cover (%) × 0.5
</pre>

<h3>2. Biomass Loss</h3>
<p>
Fire-induced biomass loss was estimated using combustion efficiency:
</p>
<pre>
Biomass Loss = AGB × 0.8
</pre>

<h3>3. Carbon Emissions</h3>
<pre>
CO₂ = Biomass Loss × 3.67

CO₂e = CO₂ + (CH₄ × 28) + (N₂O × 265)
</pre>

<p><b>Emission Factors:</b></p>
<ul>
  <li>CH₄: 6.8 kg/ton</li>
  <li>N₂O: 0.2 kg/ton</li>
  <li>CO: 80 kg/ton</li>
  <li>PM₂.₅: 5.5 kg/ton</li>
</ul>

<h3>4. NDVI Recovery Model</h3>
<pre>
NDVI(t) = NDVImin + (NDVImax - NDVImin) / (1 + e^(-k(t - t0)))
</pre>

<h3>5. Biomass Recovery</h3>
<pre>
B(t) = Bmax (1 - e^(-kt))
</pre>

<h3>6. Statistical Analysis</h3>
<ul>
  <li>Mean, Standard Deviation (SD), Coefficient of Variation (CV)</li>
  <li>Paired t-test</li>
  <li>Cohen’s d (Effect Size)</li>
  <li>Pearson Correlation</li>
</ul>

<h3>7. Carbon Payback Period</h3>
<pre>
Payback Period = Total CO₂e Emissions / Annual Sequestration Rate
</pre>

<hr>

<h2>📊 Outputs</h2>
<ul>
  <li>NDVI time series (pre, during, post fire)</li>
  <li>Evapotranspiration (ET) maps</li>
  <li>Biomass loss maps</li>
  <li>Carbon emission estimates</li>
  <li>Recovery curves and metrics</li>
</ul>

<hr>

<h2>💻 Implementation</h2>
<ul>
  <li>Google Earth Engine (GEE) for data extraction</li>
  <li>Python (NumPy, Pandas, Matplotlib)</li>
  <li>Machine Learning (LSTM for NDVI forecasting)</li>
</ul>

<hr>

<h2>📈 Applications</h2>
<ul>
  <li>Forest carbon monitoring</li>
  <li>Climate change impact assessment</li>
  <li>Fire management strategies</li>
  <li>Carbon credit and VCM projects</li>
</ul>

<hr>

<h2>👨‍🔬 Author</h2>
<p>
<b>Jintu Moni Bhuyan</b><br>
M.Tech (Remote Sensing)<br>
Specialization: Forest Carbon Dynamics & AI-based Modeling
</p>

<hr>

<h2>📄 License</h2>
<p>
This project is open-source and available under the MIT License.
</p># ForestFireCarbonRecovery
