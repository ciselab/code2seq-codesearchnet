# Comment Experiment: Documentation Generation with CodeSearchNet

This is the repository to run the experiment of code2seq on CodeSearchNet dataset for the task of Documentation Generation.

Before running this, please make sure that code2seq's master branch is up to date with our recent changes **(it currently isn't)**

## Running the experiment

To run the experiment, please first run ```prepare.sh``` or ```prepare_minimal.sh```. This will download and prepare the full and minimal datasets, respectively.

Then build the Docker image situated in code2seq directory:

```
cd code2seq
docker build -t ciselab/code2seq:latest . 
```

Lastly, run the experiment with docker-compose:

```
docker-compose up
```
