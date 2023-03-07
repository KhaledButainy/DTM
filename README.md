# DTM - Drones' Traffic Management System

This repository contains the web application for the Drone Traffic Management system. The project is my Senior Design Project which was presented as a requirement for the Computer Engineering program at KFUPM.


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.
See deployment for notes on how to deploy the project on a live system.

### Installation
* Clone the repository using the following command:

```
git clone https://github.com/KhaledButainy/DTM.git
```

* It is recommended that you create a new environment and install all the requirements there. Create a new conda environment using the following command:

```
conda create --name <myenv>
```
* Replace <myenv> with whatever name you like. Then activate the environment using the following command:

```
conda activate <mynenv>
```
* Now you need to install the requirements inside this environment. Use the following command to do so:

```
pip install -r requirements.txt
```

### Configuration

* Before running the DTM web application, make sure you add your own credentials to the config file as the following:

```
{
    "ADMINS": [
        {
            "username": "admin",
            "email": "admin@dtm.com",
            "password": "admin"
        }
    ],

    "SECRET_KEY": "Generate a SECRET_KEY and add it here",

    "LOCAL_MONGO_URI": "mongodb://<localhost>:<port>/<db_name>",
    "ATLAS_MONGO_URI": "<your_atlas_mongo_uri>",
    "STITCH_APP_ID": "<your_stitch_app_id>",
    "DATABASE_NAME": "<db_name>",

    "MAPBOX_ACCESS_TOKEN": "<mabbox_access_token>",
    "MAPBOX_STYLE": "<mapbox_style>",

    "BROKER_ADDRESS": "<broker_address>",
    "BROKER_PORT": <broker_port>,
    "BROKER_CLIENT_USERNAME": "<broker_client_usr_name>",
    "BROKER_CLIENT_PASSWORD": "<broker_client_password>"


}

```

### Run the application
* Make sure your cluster on MongoDB is up. If you have done the configuration step, make sure you are in the same directory where (run.py) is, then run the following command to run the app locally:

```
python3 run.py
```

## Built With

* [Flask](https://flask.palletsprojects.com/en/2.2.x/) - The web framework that was used
* [Bootstrap](https://getbootstrap.com/) - The styling library that was used
* [MongoDB](https://www.mongodb.com/) - The database that we used for NoSQL objects and data streaming.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* [PathPlanning](https://github.com/zhm-real/PathPlanning) - Used to find the path and upload it to the drone.
