##  Dockerfile reference

### What is dockerfile?
- Docker file is text document file which contains sequential series of commands to build an image
- The commands which user could call on command line
- These commands executed in the order in which they have written
- All these commands get executed on the base image
- Docker file must begin with `FROM` instruction/command


### Dockerfile components
- **FROM**
  - The FROM instruction initiated setup new base image to execute subsequent instructions
  - The valid Dockerfile must begin with `FROM` instruction
  - _Syntax_: `FROM <image_name>:<version>`
- **CMD**
  - The `CMD` commands defines default command to run when container starts
  - Sets default parameters that can be overridden from the Docker Command Line Interface (CLI) when a container is running
  - Syntax: `CMD <command>`  e.g: `CMD python app.py`
- **RUN**
  - The `RUN` command allows to install application and the required packages for it
  - It executes any command(Shell commands) on top of base image and creates new layer giving the result
  - _Syntax:_ `RUN <comomand>` e.g: `RUN pip install -r requirements.txt`
- **ENTRYPOINT**
  - The `ENTRYPOINT` is same as `CMD`
  - The difference is `ENTRYPOINT` allows to give extra argument to given command
  - Default parameters that cannot be overridden when Docker Containers run with CLI parameters
  - _Syntax_: `ENTRYPOINT ["echo", "Hello, Shri"]`
- **WORKDIR**
  - The `WORKDIR` instruction sets working directory to run other instructions like: RUN, CMD, ENTRYPOINT, COPY
  - Syntax: `WORKDIR </paht/to/workdir>`
- **COPY**
  - The `COPY` instructions copy files and directories from host machine(source) to container file system(destination)
  - _Syntax_ : `COPY <Host/source/path>  <container/destination/path>`
- **ARG**
  - The `ARG` instruction help to define variables at image build time
  - `ARG` values not available once image get created
  - The running container can't access its value
  - _Syntax_: `ARG <variable_name> <variable_value>`
- ENV
  - The `ENV` instruction helps to define default variables to use after container starts
  - Running dockerized application can access `ENV` variables
  - _Syntax_: `ENV <variable_name> <variable_value>`


### CMD vs ENTRYPOINT
- TODO


### ARGS vs ENV
- TODO