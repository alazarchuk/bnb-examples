# Installation
AutoAWQ, at the moment of writing, doesn't support Python 3.12, so I have to resort to conda:
```
conda create --prefix ./.cenv python=3.11
conda activate ./.cenv
```

# Issue
Unfortunately, AutoAWQ has a strict restriction on CUDA Compute Capability 7.5. In my case, neither Tesla M40 nor P40 meet this requirement, 
so as a result, inference doesn't work and raises an exception:

```
RuntimeError: CUDA error: no kernel image is available for execution on the device
```

But despite this quatization was working (I assume :) and in an hour time I had quatized Mistral 7B.