# Stationeers server that runs inside a Docker container

*Show your support for this project by signing up for a [free Bitrise account!](https://app.bitrise.io?referrer=02c20c56fa07adcb)*

**NOTE**: This image will install/update on startup. The path ```/steamcmd/stationeers``` can be mounted on the host for data persistence.

## How to run the server

1. Set the environment variables you wish to modify from below
2. Optionally mount ```/steamcmd/stationeers``` somewhere on the host or inside another container to keep your data safe
3. Enjoy!

*You might alternatively edit `default.ini` to further customize your installation, but this hasn't been fully tested. Using environment variables is the only recommended way at the moment.*

The following environment variables are available:
```
STATIONEERS_SERVER_STARTUP_ARGUMENTS (DEFAULT: "-autostart -nographics -batchmode" - Default startup arguments)
STATIONEERS_SERVER_NAME (DEFAULT: "A Docker Server" - Publicly visible server name)
STATIONEERS_WORLD_NAME  (DEFAULT: "docker" - World name, mainly used for save names etc.)
STATIONEERS_SERVER_SAVE_INTERVAL (DEFAULT: "300" - Automatic save interval in seconds)
STATIONEERS_GAME_PORT (DEFAULT: "27500" - Used for both incoming client connections (UDP) and the web-interface (TCP))
STATIONEERS_QUERY_PORT (DEFAULT: "27015" - Steam query port (UDP))
STATIONEERS_SERVER_PASSWORD (DEFAULT: "" - Server password)
```

## Administering the server

Stationeers comes with a built-in web-interface for RCON, which can be accessed at http://your-server-ip:27500.

You should definitely set/change the RCON password for this (default password is `stationeers`, which is found in `default.ini`).

## Anything else

If you need help, have questions or bug submissions, feel free to contact me **@Dids** on Twitter.

## License

See [LICENSE](LICENSE).
