# How to run it

This project provides source code to bootstrap a local deployment over docker.

**Assuming you have read [README.md](README.md) and are already comfortable about what the project does and what would be the expected outcome from this project**

# Setup and Configuration for Local Deployment

This source repository encapsulates various repositories as submodules. We will start by cloning the code to the local machine.

```
git clone --recurse-submodules -j8 git@github.com:samueljazzjohn/faceinsight-sandbox.git
```

If a new submodule is added to Sandbox, run the following commands to pull the submodule changes from Sandbox:
```
git submodule update
```

After cloning the source, to start the Docker services, run:
```
docker-compose up --build -d
```

# How to Test
This project creates various services, some of which are exposed using Traefik.

To test the successful deployment, visit:

- http://app.localhost for faceinsight dashboard
- http://api.localhost/docs for faceinsight backend service
- http://localhost:8080 for traefik service