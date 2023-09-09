# Docker-Based Jellyfin Media Server for Mac
> :apple: This is specifically designed to run on macOS

This project provides a basic **scripted**
[Jellyfin Media Server](https://jellyfin.org/)
in the project's directory using the official Jellyfin Media Server
image and Docker Compose.

---

## To Use
Just `git clone` and run the scripts.

It has three idempotent and non-destructive scripts:
  1. Run `make-jellyfin` **once** to create your Jellyfin Media Server
  2. Run `run-jellyfin` to run your Jellyfin Media Server
  3. Run `stop-jellyfin` to stop your running Jellyfin Media Server

> This setup is for access for the **internal network only!**

### To Setup the Jellyfin Media Server...
You should only need to create your Jellyfin Media Server once.

#### Prerequisites
  1. **Jellyfin Server Media Directory** - You must know and be
     able to provide the directory path to your media that
     you want to serve

To use this...
  1. Open a terminal window
  2. Git Clone this project in desired location
  3. Change directory to the project
     ```bash
     cd mac-docker-jellyfin
     ```
  4. Run the `./make-jellyfin` script and follow the prompts
     to create the Jellyfin Media Server Data Directories
     and `.env` file for the Docker Compose orchestration
     ```
     ./make-jellyfin
     ```

### To Run the Jellyfin Media Server...
Once you have created a Jellyfin Media Server, you can run and stop
it as many times as you want.

#### Prerequisites
  1. **Docker**  - You must have Docker installed
     and running
  2. **Jellyfin Server Media** - You must have the media
     that you want to serve and ideally in the Jellyfin format

#### Run
To Run your Jellyfin Media Server...
  1. Start Docker and wait until it is fully up and running
  2. You will need a browser to manage your Jellyfin Media Server
  3. Run the `./run-jellyfin` script to run the Jellyfin Media Server
     using your `.env` file
     ```
     ./run-jellyfin
     ```

     The script will open your default browser to the Jellyfin
     Media Server Wed interface at http://localhost:8096/

> :point_right: You should always be able to reach your running
> Jellyfin Media Server at http://localhost:8096/

#### Stop
To stop your Jellyfin Media Server...
  1. Run the `./stop-jellyfin` script to stop your
     Jellyfin Media Server
     ```
     ./stop-jellyfin
     ```

### To PERMANENTLY DESTROY the Jellyfin Media Server...

> :warning: **WARNING:** This action can not be undone!

To permanently destroy a created Jellyfin Media Server but keep these
project files, use the `.destroy-jellyfin` script.

  1. Run the `./destroy-jellyfin` script and follow the prompts
     to destroy your Jellyfin Media Server
     ```
     ./.destroy-jellyfin
     ```
