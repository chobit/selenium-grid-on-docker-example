# selenium-grid-on-docker

To test that, you can start a fresh linux machine (or not, your call) and hit:

$ git clone https://github.com/chobit/selenium-grid-on-docker-example.git grid && cd grid && sudo ./install.sh

This will download the scripts and install docker and docker compose.
When you install Docker, it will suggest you to add your user to the docker group. You should really do that. I help you, it’s something like this:

$ sudo usermod -aG docker your-username
Now, let’s put it to run:

$ ./run.sh

This command will pull and run 3 containers: hub, firefox and chrome. You can scale things up with:

$ ./scale.sh 10

This will scale the grid to 10 Chrome containers and 10 Firefox containers (be advised that it will eat a lot memory - it’s 20 browsers, after all).
