# ASTRA-sim 2.0
[ASTRA-sim](https://astra-sim.github.io/) is a distributed machine learning system simulator developed by Intel, Meta, and Georgia Tech. It enables the systematic study of challenges in modern deep learning systems, allowing for the exploration of bottlenecks and the development of efficient methodologies for large DNN models across diverse future platforms.

The previous version, ASTRA-sim 1.0, is available in the `ASTRA-sim-1.0` [branch](https://github.com/astra-sim/astra-sim/tree/ASTRA-sim-1.0).

Here is a concise visual summary of our simulator:
![alt text](https://github.com/astra-sim/astra-sim/blob/master/docs/images/astrasim_overview_codesign.png)

For a comprehensive understanding of the tool, and to gain insights into its capabilities, please visit our [website](https://astra-sim.github.io/).

For information on how to use ASTRA-sim, please visit our [Wiki](https://astra-sim.github.io/astra-sim-docs/index.html).

ASTRA-sim accepts Chakra Execution Traces as workload-layer inputs. For details, please visit [Chakra Github](https://github.com/mlcommons/chakra).

We appreciate your interest and support in ASTRA-sim!

## Contact Us
For any questions about using ASTRA-sim, you can email the ASTRA-sim User Mailing List: astrasim-users@googlegroups.com

To join the mailing list, please fill out the following form: https://forms.gle/18KVS99SG3k9CGXm6

## Build Instructions

1. Clone repository and build docker image
```sh
git clone --recursive https://github.com/jkrbs/astra-sim.git
docker build -t astra-sim
```

2. Enter docker container 
```sh
docker run -ti -v .:/app/astra-sim astra-sim bash
```


3. Install Chakra inside docker container and generate traces
```sh
cd extern/graph_frontend/chakra/
pip3 install .
chakra_generator
```

4. Use astra-sim
```sh
cd examples/network_analytical/
./run_network_analytical.sh
```

