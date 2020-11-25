<!-- export package info -->
conda env export > environment.yml


conda env create -f environment.yml -p newname


<!-- update all pip package -->
pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U

<!-- update all conda package -->
conda update --all
