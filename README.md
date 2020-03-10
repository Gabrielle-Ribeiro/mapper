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
docker run --rm -it -v ${PWD}:/current_dir -w /current_dir alicevision/meshroom

# Launch a 3D reconstruction
python bin/meshroom_photogrammetry --input test_3d_meshroom/input_images --output test_3d_meshroom/output
```
