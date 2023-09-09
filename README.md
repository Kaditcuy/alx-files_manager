# Files manager

## A simple platform where users sign in and can then view files or upload files using nodejs ans express js framework

### `Technology stack`

- **NodeJs**
- **ExpressJs**
- **MongoDB**
- **Redis**
- **pagination**

### `Objective is to build a simple platform to upload and view files`. Its features are:
```
* User authentication/signining in via a token.
* List all files in the system.
* Upload a new file.
* Change permissions of a file.
* View a file.
* Generate thumbnails for images (i.e previewing a file).
```

`Aim of this project` : Its a summary of core backend technologies, which includes concepts like authentication, nosql database, caching, pagination, background processes(kue) as well as object oriented programming to model the file system :).

## `Learning Objective`
```
* how to create an api with express
* how to authenticate a user
* how to store data in mongodb
* how to cache data in redis
* how to setup and use a background worker
```

`**File Structure**`
[server.js](/alx-files_manager/server.js) -> Contains server/app configuration as well as the api routes and middleware
[controllers/](/alx-files_manager/controllers/) -> Contains buisness logic functions such as user management, files management, authmanagement, app managemnt. LIke creating a user ans storing in a database kinda logic and like uploading a file and viewing files kinda logic.
[routes/](alx-files_manager/routes/) -> Contains an index.js file that houses all the apps endpoints in other words the api of the app. Nb: On each route a buisness logic function from the controllers is called.
[tests/](alx-files_manager/tests) -> Contains unittests for different componets of the app and also integration tests.
[utils/](alx-files_manager/utils/) -> Contains helper functions used throughout the app such as db.js which creetes a dbclient that can be used to add Objetcs to our databse and also execute queries throughout the app, redis.js where a redis client is created for caching operations.
[worker.js](alx-files_manager/worker.js) -> Contains code that defines two separate queues(`thumbnailQueue` and `userQueue`.These queues are designed to work asynchronously and are often used in apps that require background job processing, such as image processing and user notification.
