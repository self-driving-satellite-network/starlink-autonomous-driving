## Figure 33: Topology updates in various schemes.

<div align=center><img src="./figure33.png" width=""></div>

<table>
<thead>
  <tr>
    <th> Networking scheme</th>
    <th> Avg. num. snapshots/day</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>4-ISL(proactive)</td>
    <td>64.13</td>
  </tr>
  <tr>
    <td>n-ISL(proactive)</td>
    <td>51.29</td>
  </tr>
  <tr>
    <td>4-ISL(reactive)</td>
    <td>8.16</td>
  </tr>
  <tr>
    <td>n-ISL(reactive)</td>
    <td>5.92</td>
  </tr>

</tbody>
</table>

### Overview
Figure 33 shows topology updates in various schemes.


### Experimental methodology
Our experiments are based on Two-line elements from space-track.org.


### How to run the code
```
jupyter notebook
open figure33.ipynb file and run notebook
```

### Data
The data can be found in the `figure33/` folder.

	|- figure33
		|- data
			|- snap_gnp.npy
			|- ...