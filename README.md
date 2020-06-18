### Setup and running the analysis
If you have jupyter notebook already—you're good to go. If not then you might prefer a docker based setup to avoid installing jupyter notebook and setting up python virtual envs and the accompanying pain.

#### Jupyter notebook
1. Clone the the repo into [some_directory]
2. Run `pip install pandas scipy matplotlib pytrends googletrans`
3. Start jupyter notebook and open either the anosmia.ipynm or loss_of_smell.ipynb
4. Run all the cells top to bottom

#### Docker setup
1. Clone the repo into [some_directory]
2. Run `docker run -p 8888:8888 -v ~/[some_directory]:/home/jovyan jupyter/scipy-notebook`
3. The terminal output will contain a link starting with `http://localhost:8888/?token=...`, open this in a new browser window
4. Get the CONTAINER ID of the running container by running `docker ps` in a new terminal window
5. Install other required packages to the container by running `docker exec [CONTAINER ID] pip install pytrends googletrans`
6. Go back to the browser window and open anosmia.ipynb or loss_of_smell.ipynb
4. Run all the cells top to bottom
