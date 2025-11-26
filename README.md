this is a two stage build for an audiocraft environment on the dgx spark. 

it took me a long time to get this right. 

first, run this:

```
docker build -t thecollabagepatch/torch-cudnn:latest -f Dockerfile.torch-cudnn .
```

it will take a long time. 

then you can build the audiocraft runtime on top of this base image. 

```
docker build -t thecollabagepatch/audiocraft-runtime:lattest -f Dockerfile.audiocraft-runtime .
```

it's been almost a month since i built both of these. i can enter the container and run training as well as inference. i really hope this works for you.

i will update this with easy-to-use training scripts as well shortly, using this colab notebook as a guide. 

https://colab.research.google.com/gist/fyremael/c85df73487ab8bec51fe421723dd9606/audiocraftwerk_v0-2-1-1.ipynb

shoutout baltigor. 