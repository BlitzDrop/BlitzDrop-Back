# BlitzDrop API Backend
After cloning the repository 
```
git clone https://github.com/BlitzDrop/BlitzDrop-Back
```

You must create a .env file like:
```
JWT_SECRET=secret_jwt_key


CLIENT_ID=client_id
CLIENT_SECRET=secret_client
```

Then, to launch the API:
```
docker compose up --build -d
```
Visit http://localhost:3000/ in your browser to check if backend is working, browser must shows *BlitzDrop API working!*. Be sure you have waited 2 or 3 minutes before checking 
the server.

You can also launch **MongDB Express** client searching http://localhost:8081 in your browser. This will pop up a window requesting an user and password,
you must enter:

```
user: admin
password: password123
```

In the other hand, if the server have been successfully initialized, you can check BlitzDrop API docs via http://localhost:3000/openapi.

Docker will launch seeders after initializing the database but in case you execute http://localhost:3000/items and it returns an empty list, execute the endpoint
http://localhost:3000/seed.

If anything goes wrong or you want to restart the container, you can launch

```
docker compose down -v
docker compose up --build -d
```

This will delete the entire MongoDB database and restart every collections and launch the container again.
