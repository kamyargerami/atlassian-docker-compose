# Atlassian Jira + Confluence with Docker and docker-compose

This project run & Activate (crack) Atlassian software as docker container, All programs can be run behind a reverse proxy.

## Run Application
- Install docker and docker-compose.
- Clone this project
- Copy `.env.example` to `.env`
- Edit `.env` file as you need - you need to edit final url and port
- Run docker-compose as below:

```
docker-compose up -d
```

## Activation
If you need to activate the applications you can get the code by running this command:

### Jira software

```
docker-compose exec jira java -jar /agent.jar -d -m my@email.com -o mycompany -p jira -s <SERVER_ID>
```

### Confluence

```
docker-compose exec confluence java -jar /agent.jar -d -m my@email.com -o mycompany -p conf -s <SERVER_ID>
```

## Troubleshooting

### Version
If activation doesn't work on latest version you can change it as below:

Last version for jira-software that I checked: 8.22.5

Last version for confluence that I checked: 8.3.2