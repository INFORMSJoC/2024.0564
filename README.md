[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

# On the Instance Dependence of Parameter Initialization for the Quantum Approximate Optimization Algorithm: Insights via Instance Space Analysis

This archive is distributed in association with the [INFORMS Journal on
Computing](https://pubsonline.informs.org/journal/ijoc) under the [MIT License](LICENSE).

The software and data in this repository are a snapshot of the software and data
that were used in the research reported on in the paper 
[On the Instance Dependence of Parameter Initialization for the Quantum Approximate Optimization Algorithm: Insights via Instance Space Analysis](DOI_MISSING) by Vivek Katial, Kate Smith-Miles, Charles Hill and Lloyd Hollenberg.

## Cite

To cite the contents of this repository, please cite both the paper and this repo, using their respective DOIs.

https://doi.org/DOI_MISSING/ijoc.2024.0564

Below is the BibTex for citing this snapshot of the repository.

```
@misc{Katial2024,
  author =        {Katial, Vivek and Smith-Miles, Kate and Hill, Charles and Hollenberg, Lloyd},
  publisher =     {INFORMS Journal on Computing},
  title =         {{On the Instance Dependence of Parameter Initialization for the Quantum Approximate Optimization Algorithm: Insights via Instance Space Analysis}},
  year =          {2024},
  doi =           {DOI_MISSING/ijoc.2024.0564},
  url =           {https://github.com/INFORMSJoC/2024.0564},
  note =          {Available for download at https://github.com/INFORMSJoC/2024.0564},
}  
```

## Description

This repository contains the code for the experiments in the paper "On the Instance Dependence of Parameter Initialization for the Quantum Approximate Optimization Algorithm: Insights via Instance Space Analysis" by Vivek Katial, Kate Smith-Miles, Charles Hill and Lloyd Hollenberg.

## Running with Docker

You are able to run the code in this repository with Docker. The following instructions assume that you have Docker installed on your machine (e.g. [Docker Desktop](https://www.docker.com/products/docker-desktop/)).

```
docker build -t qokit .
```

Run the container with the following command:
```
docker run -p 8888:8888 qokit
```

Run the container with the following command to mount the current directory:
```
docker run -v $(pwd):/app -p 8888:8888 qokit
```

Run the instance and add .env file and mount the current directory:
```
docker run -v $(pwd):/app --env-file .env -p 8888:8888 qokit
```

Once running, you can SSH into the container with the following command:
```
docker exec -it <container_id> /bin/bash
```

Once inside the container, you can run the following command to run an experiment:

```
python run_instance.py
```

## Running with Apptainer

You are able to run the code in this repository with Apptainer. The following instructions assume that you have Apptainer installed on your machine (e.g. [Apptainer](https://apptainer.org/docs/user/installation.html)). Apptainer is a containerization tool that is designed for high-performance computing environments.

```
apptainer build qaoa.sif apptainer.def
```

## Results

The results in our publication can be found in the `results` folder -- the main results for the ISA experiments can be found in `results/isa-plots` and the performance analysis plots can be found in `results/performance-analysis`.



## Data Access

For accessing the studied in our publication, please see the folder `data/isa-instances`. The instances are in the format of `.graphml` files. We also provide the metadata for the instances in `data/metadata.csv` and the results from the ISA in `data/MATILDA`.

## Acknowledgement

This software was developed on top of [QOKit](https://github.com/jpmorganchase/QOKit)