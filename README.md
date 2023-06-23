python anomaly_detection.py

<p>This will read the data from the wireshark_dataset.csv file and print out the detected anomalies.</p>

<h2>How to Use</h2>

<p>The project can be used to detect anomalies in any type of network traffic data. To use the project, you will need to provide the following:</p>

<ul>
<li>The path to the data file</li>
<li>The threshold value for the MSE</li>
</ul>

<p>The data file should be a CSV file with the following columns:</p>

<ul>
<li>Protocol</li>
<li>Length</li>
</ul>

<p>The threshold value is a percentile value that determines which data points are considered to be anomalies. For example, if the threshold value is set to 95, then the 5% of data points with the highest MSE values will be considered to be anomalies.</p>
