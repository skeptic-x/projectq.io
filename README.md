# Dev Setup

1. Create Python Environment:  
`python3 -m venv .venv`
2. Activate Environment:  
`source .venv/bin/activate `
3. Install requirements:  
`pip install -r requirements.txt`

# Misc

# Build Site
`mkdocs build`
# Serve Site
`mkdocs serve`
# Deploy Site
`mkdocs gh-deploy -c -m "projectq.io website update." --force --no-history`


# NOCODB
create '.env' file in `nocodb` with 
```shell
POSTGRES_PASSWORD=some-db-password
NC_ADMIN_PASSWORD=some-ui-password
NC_AUTH_JWT_SECRET=some-jwt-secret
```
`cd nocodb`  
`docker-compose up -d`  

