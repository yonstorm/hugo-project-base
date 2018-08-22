# Hugo development template

## Usage 
Have Docker installed

Clone this repository and run:
```bash
CURRENT_UID=$(id -u):$(id -g) docker-compose up
```

### Running Hugo commands inside the container

```bash
docker exec -d -w /opt/site hugo_site_dev COMMAND 
``` 

## Structure

```
|--site                // Everything in here will be built with hugo
|  |--content          // Pages and collections - ask if you need extra pages
|  |--data             // YAML data files with any data for use in examples
|  |--layouts          // This is where all templates go
|  |  |--partials      // This is where includes live
|  |  |--index.html    // The index page
|  |--static           // Files in here ends up in the public folder
|--src                 // Files that will pass through the asset pipeline
|  |--css              // CSS files in the root of this folder will end up in /css/...
|  |--js               // app.js will be compiled to /app.js with babel
```
