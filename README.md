Create venv for Python 3.10+

`python3 -m venv .venv`

Install requirements

`pip install -r requirements.txt`

Pull the Postgres Docker Image with `docker pull postgres`

Create a Docker Volume `docker volume create postgres_data`

Run the Postgres Docker Container `docker run --name postgres_container -e POSTGRES_PASSWORD=pass -d -p 5432:5432 -v postgres_data:/var/lib/postgresql/data postgres`

`docker ps -a` to verify container is running

Run `flask-run.sh`

Check api with `curl localhost:5000/plants`
