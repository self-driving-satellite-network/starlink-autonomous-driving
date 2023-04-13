# A Networking Perspective on Starlink’s Self-Driving LEO Mega-Constellation

This repository collects the artifacts of the MobiCom'23 paper "A Networking Perspective on Starlink’s Self-Drivincg LEO Mega-Constellation."

<div align=center><img src="./overview.png" width="100%"></div>


## Overview
Low-earth-orbit (LEO) satellite mega-constellations, such as SpaceX Starlink, are under rocket-fast deployments and promise broadband Internet to remote areas that terrestrial networks cannot reach. For mission safety and sustainable uses of space, Starlink has adopted a proprietary onboard autonomous driving system for its extremely mobile LEO satellites. This paper demystifies and diagnoses its impacts on the LEO mega-constellation and satellite networks. We design a domain-specific method to characterize key components in Starlink’s autonomous driving from various public space situational awareness datasets, including continuous orbitmaintenance, collision avoidance, and maneuvers between orbital shells. Our analysis shows that, these operations have mixed impacts on the stability and performance of the entire mega-constellation, inter-satellite links, topology, and upper-layer network functions. To this end, we investigate and empirically assess the potential of networking-autonomousdriving co-designs for the upcoming satellite networks






## Repository structure

This repository includes the following contents:

	|- MobiCom23
		|- Dataset
			|-Starlink-TLE: Two-line elements of Starlink satellites.
			|-Conjunction-data: Conjunction report
		|- Figures-and-Tables: Source files of figures and tables in [1]
			|-Figure4
			|-Figure6
			|-Table2
			|-...
		|- Space-debris.png: Space debris.
		|- Space-threats.png: Space threats.
		|- Starlink-maneuver-overview.png: Starlink maneuver overview.
		|- overview.png: Overview.
		|- Mobicom23.pdf: The MobiCom'23 paper.
		|- README.md: This file.
  


​	
## Dataset


We use two datasets for the empirical study and evaluation (in `MobiCom23/Dataset/`):

- **Starlink TLE**: The dataset is collected from space-track.org
- **Conjunction data**: The dataset is collected from celestrack.org
  

<table align="center">
<thead>
  <tr>
    <th> Dataset Type</th>
    <th> Starlink TLE</th>
    <th> Conjunction data</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Dataset Source</td>
    <td>space-track.org</td>
    <td>celestrak.org</td>
  </tr>
  <tr>
    <td>Time Range</td>
    <td>2019/05-2022/07</td>
    <td>2022/04-2022/07</td>
  </tr>
  <tr>
    <td>Num. entries</td>
    <td>41,188,538</td>
    <td>9,350,134</td>
  </tr>
  <tr>
    <td>Entry interval</td>
    <td>3.0-34.7 hrs</td>
    <td>8 hrs</td>
  </tr>
   <tr>
    <td>Num. space objects</td>
    <td>24,237</td>
    <td>21,743</td>
  </tr>
  <tr>
    <td>Orbit altitudes</td>
    <td>162-575,074 km</td>
    <td>239-91314 km</td>
  </tr>
  <tr>
    <td>Orbit inclinations</td>
    <td>0-145°</td>
    <td>0-145°</td>
  </tr>
</tbody>
</table>


## Figures and Tables

In `MobiCom23/Figures-and-Tables/`, we release the traces used in [1]'s figures and tables, including

- `Figure4`: Distribution of space objects by altitudes
- `Figure6`: An example of Starlink satellite’s maneuver behaviors
- `Figure8a`: Space objects in our dataset.
- `Figure8b`: SGP4 accuracy w/o maneuvers
- `Figure9`: Orbital parameter distributions in dataset
- `Figure10`: Statistics of conjunction events
- `Figure11`: Inferring satellite neighborship by RAAN.
- `Figure12a`: The necessity of orbit maintenance.
- `Figure12b`: Heterogeneous orbital decays if w/o orbit maintenance in Starlink.
- `Figure12c`: Orbital decays around Iridium
- `Figure12d`: Orbital decays around Oneweb
- `Figure13`: Deviations of LEO orbital parameters.
- `Figure14`: Neighborship updates w/o maintenance.
- `Figure15`: Orbit maintenance’s impacts on ISLs.
- `Figure16`: Orbital maintenance facilitates ISL stability.
- `Figure17`: Orbital decay’s impacts on 1,000 randomly distributed inter-satellite network traffic flows.
- `Figure18`: Classification of collision avoidance in Starlink’s autonomous driving (the solid green line).
- `Figure19b`: A 3D view of Starlink’s collision avoidance maneuver in Figure 18a in the RTN coordinate system.
- `Figure20`: Collision risks between space objects.
- `Figure21`: Effectiveness of collision avoidance.
- `Figure22`: Cooperative Starlink-Starlink maneuver.
- `Figure23a`: A showcase of unnecessary maneuver.
- `Figure23b`: Statistical characteristics of unnecessary collision avoidances.
- `Figure24`: Starlink’s high-risk orbital maneuver.
- `Figure25`: ISL’s out-of-alignment by maneuvers
- `Figure26`: Starlink’s maneuvers between multiple orbital shells.
- `Figure27`: A showcase of inter-orbit-shell maneuver.
- `Figure28`: The number of satellites conducting interorbit-shell maneuvers per day.
- `Figure30`: Satellite neighborship updates per day.
- `Figure31`: ISL’s length and delay under maneuvers.
- `Figure32`: ISL updates in various networking schemes.
- `Figure33`: Topology updates in various schemes.
- `Figure34`: ISL delay in various networking schemes.
- `Figure35`: ISL failures in various networking schemes.
- `Figure36`: Traffic performance in various schemes.
- `Table2`: Duration and extent of collision avoidances.

Each table/figure has a `README.md` in its corresponding folder that details the experimental methodology and how to run the code.

## Dependencies

To run all code in this repository, please use `python3 + jupyter notebook` and install the following packages:

```
pip3 install matplotlib numpy statsmodels pandas scipy seaborn tqdm skyfield TLE-tools xlrd pytz
```

<!-- ## Raw dataset access
Due to excessive data volume, we do not intend to release all raw data here and put a sample in the dataset folder. If you want more data, please send a request to yuanjiel@tsinghua.edu.cn.

The request should include the work department, the purpose of data usage, and the data content obtained. -->

## Citation

Please indicate this repository when using it and cite our MobiCom paper [1].

## Contact

Please contact yuanjiel@tsinghua.edu.cn for any questions or technical support.


## References

[1] A Networking Perspective on Starlink’s Self-Driving LEO Mega-Constellation. To appear at ACM MobiCom 2023.
