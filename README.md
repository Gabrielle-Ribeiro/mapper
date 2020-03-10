# mapper
2D and 3D mapping with third-party libraries
## How to install
#### If your machine is CUDA enabled, just
```
docker pull alicevision/meshroom
```
#### Else, just cry. Kidding. Use another machine or a cloud service.

## How to run
```
# Choose a dataset from photogrammetry_dataset_links
# Put the images from the dataset in the mapper/test_3d_meshroom/input_images folder

# Access this repo directory from the terminal
cd mapper

# Run the container
docker run -v ${PWD}:/current_dir -w /current_dir --net=host --env="DISPLAY" --volume="$HOME/.Xauthority:/root/.Xauthority:rw" --rm -it --runtime=nvidia alicevision/meshroom
## Explanation of the unusual parameters
### Use your current folder as a volume
-v ${PWD}:/current_dir -w /current_dir
### Make the docker container able to display GUI apps
--net=host --env="DISPLAY" --volume="$HOME/.Xauthority:/root/.Xauthority:rw"

# Launch a live 3D reconstruction
## Open meshroom GUI app
meshroom
## Follow the following tutorial:
```
##### [Live Reconstruction Tutorial with Meshroom](https://meshroom-manual.readthedocs.io/en/latest/gui/live-reconstruction/live-reconstruction.html)
```
## Add the dataset images to the input folder one by one
```
