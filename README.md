RIPE Atlas Toolbox
=====================

Atlas Toolbox is a collection of Perl command-line scripts from managing custom User Defined Measurements (UDMs) on the **RIPE Atlas** network.

Atlas is a large measurement network composed of geographically distributed probes used to measure Internet connectivity and reachability.

This toolbox allow to search probes on the network, visualize public measurements set by other Atlas users, configure custom active measurements and get their results. The scripts use Atlas' REST APIs.

#### List of scripts

- **probe-list**: search probes on the network
- **udm-create**: set up a custom measurement (ping/traceroute/dns)
- **udm-status**: check status of a measurement
- **udm-result**: retrieve results of a measurement
- **udm-stop**: stop a running measurement
- **udm-lookup**: search existing measurements

----------

Prerequisites
-------------

To run the scripts, the Perl interpreter is needed (it comes pre-installed on most systems). 
Additional PERL modules are used, such as HTTP::Request, HTTP::Response, LWP::UserAgent, LWP::Sumple, JSON and Geo::Coder.

The last two might might need to be manually installed via the OS packet manager or CPAN, as showed below.

#### Debian/Ubuntu systems

```
sudo apt-get install libjson-perl
sudo apt-get install libgeo-coder-googlev3-perl
```

#### Using CPAN (multi-platform)

```
sudo perl -MCPAN -e shell
install JSON
install Geo::Coder::Googlev3
```

Check here how to install Perl modules: <http://www.cpan.org/modules/INSTALL.html>

Install
-------

```sh
git clone https://github.com/pierdom/atlas-toolbox
cd atlas-toolbox
```

Usage
-----

Run a script:

```
perl <script-name> [OPTIONS]...
```

Every scripts comes with its own documentation. To have a list of all available options use --help option; to reed the full documentation:

```sh
perldoc <script-name>
```

License
-------

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>


Acknowledgement
---------------

This work has been partially funded by the European Commission 
funded mPlane ICT-318627 project (www.ict-mplane.eu).


Author
------

Pierdomenico Fiadino
fiadino@ftw.at
<http://userver.ftw.at/~fiadino>
