# OpenAPI generated server

## Overview
This server was generated by the [OpenAPI Generator](https://openapi-generator.tech) project. By using the
[OpenAPI-Spec](https://openapis.org) from a remote server, you can easily generate a server stub.  This
is an example of building a OpenAPI-enabled Flask server.

This example uses the [Connexion](https://github.com/zalando/connexion) library on top of Flask.

## Requirements
Python 3.5.2+

## Usage
To run the server, please execute the following from the root directory:

```
cd output/python-flask
deactivate
python3 -m venv .venv
source .venv/bin/activate
pip3 install wheel
pip3 install -r requirements.txt
python3 -m openapi_server

pip3 freeze | grep -v "pkg-resources" > requirements.txt
heroku logs --tail --app bnoteapi
```

```
export OPENAPI_FLASK_CONFIG_FILE="/home/[user]/projects/tys-hiroshi/openapi3-codegen/output/python-flask/openapi_server/config.py"
```

and open your browser to here:

```
http://localhost:8080/v1/ui/
```

Your OpenAPI definition lives here:

```
http://localhost:8080/v1/openapi.json
```

To launch the integration tests, use tox:
```
sudo pip install tox
tox
```

## Running with Docker

To run the server on a Docker container, please execute the following from the root directory:

```bash
# building the image
docker build -t openapi_server .

# starting up a container
docker run -p 8080:8080 openapi_server
```


```
sudo apt install -y nodejs npm
sudo npm install n -g
sudo n stable
sudo apt purge -y nodejs npm
exec $SHELL -l
node -v
sudo n lts
sudo npm install -g openapi-to-postmanv2
openapi2postmanv2 -s openapi_server/openapi/openapi.yaml -o postman_collection.json -p
```

