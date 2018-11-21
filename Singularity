From:nfcore/base
Bootstrap:docker

%labels
    DESCRIPTION Singularity image containing all requirements for the nf-core/dda-quant-proteomics pipeline
    VERSION 1.0dev

%environment
    PATH=/opt/conda/envs/nf-core-dda-quant-proteomics-1.0dev/bin:$PATH
    export PATH

%files
    environment.yml /
    tools/openms/environment.yml /openms_env.yml

%post
    /opt/conda/bin/conda env create -f /environment.yml
    /opt/conda/bin/conda env create -f /openms_env.yml
    /opt/conda/bin/conda clean -a
