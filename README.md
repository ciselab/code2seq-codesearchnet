# Comment Experiment: Documentation Generation with CodeSearchNet

This is the repository to run the experiment of code2seq on CodeSearchNet dataset for the task of Documentation Generation.

## Running the experiment

- First clone the repository recursively:
```
git clone git@github.com:ciselab/code2seq-codesearchnet.git --recursive
```

- Make sure you have ```nvidia-container-toolkit``` installed, this will allow your Docker containers to access your Nvidia card:
```
pamac install nvidia-container-toolkit
```
(switch pamac for a package manager that your distribution uses). If your Nvidia card still doesn't work, some troubleshooting can be found [here](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html) and [here](https://medium.com/@mmnshkmr/manjaro-setup-tensorflow-docker-container-w-nvidia-gpu-cacd0714f9b).

- To run the experiment, please first run (as root) ```prepare.sh``` or ```prepare_minimal.sh```. This will download and prepare the full and minimal datasets, respectively.

- Then run the experiment with docker-compose:
```
docker-compose up --build
```

**Warning!** If you hit the rate limits on Nvidia Docker image downloads, you might start getting an ```401 Unauthorized``` error when trying to download the Docker image. If that happens, please follow [this guide](https://stackoverflow.com/a/70970425/13988119) to register and login through your Nvidia account.
