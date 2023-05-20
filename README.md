# cicd-demo
Original source code from https://github.com/jakerieger/FlaskIntroduction and has been updated in https://github.com/cloudacode/FlaskIntroduction

## Features
- Update `SQLALCHEMY_DATABASE_URI` to implement MariaDB
- Allow anywhere host='0.0.0.0'
- Build MariaDB Container

## How To Run locally(via Docker Compose)
1. If not already done, [install Docker Compose](https://docs.docker.com/compose/install/)
2. Run `docker-compose build --pull --no-cache` to build fresh images
3. Run `docker-compose up` (the logs will be displayed in the current shell)
4. Open `https://localhost:5000` in your favorite web browser
5. Run `docker-compose down --remove-orphans` to stop the containers.

## For SQLite
```bash
python
>>> from app import app, db
>>> app.app_context().push()
>>> db.create_all()
```
