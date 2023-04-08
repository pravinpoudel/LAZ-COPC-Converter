# COPC-writer

# guide on installing pdal and using pipeline 

I encountered an issue during the initial installation when attempting to install in the base environment. There were conflicts and dependencies that I was unable to resolve, so I created a separate environment. 
If you encounter any difficulties during installation, I recommend creating a new environment.

```console

conda create -n pdalpy python=3.9

conda acivate pdalpy

conda install -c conda-forge python-pdal

 ```

to check if installation got me pdal, 

run 
```console
pdal
```

Although it may not be necessary, I opted to install PDAL (which I believe is the same as python-pdal) for added reassurance.

```console
conda install -c conda-forge pdal
```
and 

```console
conda install -c conda-forge gdal
```

The pipeline file "copc_filter.json" comprises two pipelines: one is a LAS reader and the other is a COPC writer, both of which are provided by the PDAL library.

change input and output file name you want 

To run the pipeline "copc_filter.json" that converts a LAS/LAZ file to a COPC file, you can use the following command line:


```console
pdal pipeline copc_filter.json
```

And the pipeline completed successfully, you can find the output file "output_file.copc" in the same directory where you ran the command.
