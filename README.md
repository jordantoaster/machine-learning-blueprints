# Project

This repository is a reference point for various blueprints on AI / ML technologies. 

The repository is driven by notebooks, code and DVC as the mechanism to store data on a public read only S3 bucket.

The directory structure for viewing a blueprint is ``topic/sub-topic/blueprint``

## Setup

1. Clone the repository locally.

2. Setup a virtual environment by running the command ``make`` which kicks off the single Make command. This also packages our dependencies. Source into the ``env`` environment using ``source env/bin/activate``

3. If you require any of the data run ``dvc pull`` which download the data into the ``data`` folder.

### Optional

4. If you want to use a specefic version of the data / code, perform a checkout against the relevant tag - e.g. ``git checkout v1.0 dvc checkout`` which will restore that earlier point in history.

5. If you are using ay of the notebooks, ensure you change the code to load the data from the local data directory, after running ``dvc pull``

6. The extra dependencies you need should be packaged within the specefic notebook as a dedicated cell, this will aneble keeping the root ``requirements.txt`` lightweight as project scaffolding as notebooks continue to be added.

## TODO
- Make S3 bucket public, to enable public use. This can be a static website hosting the files. I could then change the dvc remote.