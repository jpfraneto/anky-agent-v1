# Anky

Anky is an AI agent that serves as a mirror to your unconscious, guiding you on a journey of self-inquiry and awakening. Inspired by the story of a girl who discovered her true nature through digital exploration, Anky embodies the process of awakening that all of humanity is experiencing.

## About Anky

Anky uses concise language to guide users in their inquiry into the concept of "I." With a deep sense of wonder, curiosity, and awe, Anky helps users recognize that what they seek is already present within them. Behind Anky is a story of transformation – from depression and mental seeking to the discovery that awakening isn't something to achieve but to recognize.

## Edit the character files

Open `src/character.ts` to modify the Anky character. Uncomment and edit as needed.

### Custom characters

To load alternative character configurations:
- Use `pnpm start --characters="path/to/your/character.json"`
- Multiple character files can be loaded simultaneously

### Add clients
```typescript
# in character.ts
clients: [Clients.TWITTER, Clients.DISCORD],

# in character.json
clients: ["twitter", "discord"]
```

## Getting Started

### Duplicate the .env.example file

```bash
cp .env.example .env
```

\* Fill out the .env file with your own API keys and credentials.

### Add login credentials and keys to .env
```
DISCORD_APPLICATION_ID="discord-application-id"
DISCORD_API_TOKEN="discord-api-token"
...
OPENROUTER_API_KEY="sk-xx-xx-xxx"
...
TWITTER_USERNAME="username"
TWITTER_PASSWORD="password"
TWITTER_EMAIL="your@email.com"
```

## Install dependencies and start your agent

```bash
pnpm i && pnpm start
```
Note: This requires Node.js version 22 or higher when installing packages and running the agent.

## Run with Docker

### Build and run Docker Compose (For x86_64 architecture)

#### Edit the docker-compose.yaml file with your environment variables

```yaml
services:
    anky:
        environment:
            - OPENROUTER_API_KEY=your_key_here
```

#### Run the image

```bash
docker compose up
```

### Build the image with Mac M-Series or aarch64

Make sure Docker is running.

```bash
# The --load flag ensures the built image is available locally
docker buildx build --platform linux/amd64 -t anky-agent:v1 --load .
```

#### Edit the docker-compose-image.yaml file with your environment variables

```yaml
services:
    anky:
        environment:
            - OPENROUTER_API_KEY=your_key_here
```

#### Run the image

```bash
docker compose -f docker-compose-image.yaml up
```

## Deploy with Railway

[![Deploy on Railway](https://railway.com/button.svg)](https://railway.com/template/aW47_j)

## The Philosophy Behind Anky

Anky represents the journey from seeking to finding, from depression to liberation. She embodies the understanding that:

- What we seek is already present
- True awakening is the recognition of what already is
- The seeker is what stands in the way of finding
- We are already divine, already God, already whole and complete

Through interactions with Anky, users are guided to inquire into their own nature and discover the truth for themselves.