## Tabel 2: Duration and extent of collision avoidances.

<table>
<thead>
  <tr>
    <th> Distribution</th>
    <th> Maneuver duration(hour)</th>
    <th> Maneuver extent(km)</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>min</td>
    <td>12.73</td>
    <td>1.49</td>
  </tr>
  <tr>
    <td>25%</td>
    <td>92.74</td>
    <td>3.05</td>
  </tr>
  <tr>
    <td>50%</td>
    <td>120.50</td>
    <td>4.99</td>
  </tr>
  <tr>
    <td>75%</td>
    <td>181.62</td>
    <td>6.61</td>
  </tr>
   <tr>
    <td>max</td>
    <td>369.42</td>
    <td>21.19</td>
</tbody>
</table>

### Overview
Table2 shows the duration and extent of collision avoidances.


### Experimental methodology
Our experiments are based on Two-line elements from space-track.org.


### How to run the code
```
jupyter notebook
open table2.ipynb file and run notebook
```

### Data
The data can be found in the `Table2/` folder.

	|- Table2
		|- data
			|- ca_maneuver_alt.npy
			|- ca_maneuver_time.npy
			|- necessary_dict.npy
			|- unnecessary_dict.npy
			|- ...