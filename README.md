# Personal Finance App

This project is personal finance app built in React for the frontend, Spring Boot for the backend and MySql database. Docker was used for containerization. 
## Prerequisites

- Docker
- Git

## Getting Started

Follow these steps to get your development environment set up:

1. **Clone the repository with submodules**
```
git clone --recurse-submodules https://github.com/MatejaMusa/personal-finance-app-docker-compose.git
cd personal-finance-app-docker-compose
```

If you've already cloned the repository without the `--recurse-submodules` flag, you can run:
```
git submodule init
git submodule update
```

2. **Set up environment variables**
- Copy the example environment file
  ```
  cp .env.example .env
  ```
- Open the `.env` file and fill in the necessary values
- For `JWT_SECRET` go to this website: https://asecuritysite.com/encryption/plain
- Key size should be 256 bit and copy the Hex Key.
3. **Build and start the Docker containers**
```
docker compose up --build
```
## Usage

After the containers are up and running, you can access:

- Frontend: http://localhost:5173
- Backend: http://localhost:8080

## Troubleshooting

If you encounter any issues, please check the following:

1. Ensure all required environment variables are set in your `.env` file
2. Make sure no other services are running on the ports specified in the `docker-compose.yml` file
3. Verify that submodules are properly initialized and updated
4. If changes are not reflecting, try rebuilding the containers:
```
docker-compose down
docker-compose up --build
```
