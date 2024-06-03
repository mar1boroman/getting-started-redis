# getting-started-redis

# About this demo application

The ecommerce folder contains a collection of jupyter notebooks which demonstrate how ecommerce companies can leverage Redis Enterprise in different use cases


## Project Setup

### Spin up a Redis instance enabled with RedisStack!

The easiest way to is to use a docker image using the below command
```bash
docker run -d -p 6379:6379 -p 8001:8001 redis/redis-stack:latest
```

If you do not want to use a docker image, you can sign up for a free Redis Cloud subscription [here](https://redis.com/try-free).

###  Set up the project

Download the repository

```
git clone https://github.com/mar1boroman/getting-started-redis.git && cd getting-started-redis
```

Prepare and activate the virtual environment

```
python3 -m venv venv && source venv/bin/activate
```

Install necessary libraries and dependencies

```
pip install -r requirements.txt
```



### Using the project

#### Update Config

Make sure you update the first cell with appropriate hostname port and password

```python
import redis
import json

# Define connection variables
host = 'localhost'
port =  6379
password = 'mypassword'

# Connect to Redis
r = redis.Redis(host=host, port=port, password=password, decode_responses=True)
print('Connected to Redis')

r.flushdb()
```

All the notebooks can be run directly in Visual Studio Code IDE