## Fast API Random

This is a Fast API app which returns a random number to the clients.


## Steps to create the api

$ mkdir fa-random
$ cd fa-random/
$ touch main.py
$ python3 -m venv venv
$ . venv/bin/activate
(venv) $ pip install "fastapi[all]"
(venv) $ pip install requests
(venv) $ uvicorn main:app --reload
INFO:     Will watch for changes in these directories: ['/home/liam/projects/fa-random']
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [99120] using WatchFiles
INFO:     Started server process [99122]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     127.0.0.1:60398 - "GET / HTTP/1.1" 200 OK
INFO:     127.0.0.1:60398 - "GET /favicon.ico HTTP/1.1" 404 Not Found
^CINFO:     Shutting down
INFO:     Waiting for application shutdown.
INFO:     Application shutdown complete.
INFO:     Finished server process [99122]
INFO:     Stopping reloader process [99120]
$ code .

## Testing

To run api (main.py)
$ uvicorn main:app --reload

--> Now the api runs in http://127.0.0.1:8000. 

Test
http://127.0.0.1:8000
http://127.0.0.1:8000/random
http://127.0.0.1:8000/random/200

To see API documentation and built-in client app
http://127.0.0.1:8000/docs

To run the client
Make sure the api is running.
$ python3 example.py

--> it returns the json from api.
{'example': 'This is an example', 'data': 0}



