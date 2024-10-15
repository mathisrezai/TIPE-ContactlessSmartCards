<h2>Experiment Report: Communication Between Two Arduinos</h2>

<p>
  This experiment involved setting up communication between two Arduinos, where the first one sent a pulse (message sent: "MP"), and the other one received the voltage and converted it into a binary list (binary message).
</p>

<h3>Observations:</h3>
<ul>
  <li>Both codes were launched at the same time.</li>
  <li>Initial results showed failure: the first bits were not captured by the system.</li>
  <li>Hypothesis: Latency issues stemming from Python code verification and communication between Arduino and Python.</li>
</ul>

<h3>Latency Measurement:</h3>
<ul>
  <li>We attempted to measure this latency to synchronize the start of both systems.</li>
  <li>Results were inconclusive, with the number of bits not captured varying between trials.</li>
</ul>

<h3>Detection System Improvement:</h3>
<p>
  A method to detect the start of the message was implemented. The binary message was preceded by a '1' that symbolized the beginning of the transmission. This allowed us to initiate the detection process well before launching the message. The system would detect only '0's until it received the signal (i.e., the '1' preceding the binary message).
</p>

<p>
  <strong>Results:</strong> This idea worked, and the code was successfully transmitted.
</p>

<h3>Additional Step:</h3>
<ul>
  <li>A code was added to convert the binary back into a readable message.</li>
  <li>The word 'MP' was successfully received using the system.</li>
</ul>