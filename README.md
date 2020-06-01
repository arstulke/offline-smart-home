# Setup
## Mycroft
1. Pair with https://home.mycroft.ai
2. Install Mozilla IoT Skill (https://github.com/mozilla-iot/mozilla-webthings-gateway-skill)
	```
	docker container exec -it mycroft bash
	msm install https://github.com/mozilla-iot/mozilla-webthings-gateway-skill
	```
3. Don't change language settings

## Mozilla IoT Gateway
1. Open http://${HOSTNAME}.local:8080 and follow initial setup
2. Assert correct version number (v0.11.0, new versions aren't compatible with the offical mycroft skill)
3. Add devices (use virtual-things addon for testing)
4. (optional) generate developer token for local-only access

## Configure Mycroft Skill
1. Open https://home.mycroft.ai/skills
2. Select "Mozilla WebThings Gateway"
3. Select a) for remote access and b) for local-only access
	a) Use Connect button and authorize
	b) fill in the Gateway URL (use http://gateway:8080 as URL) and Developer Token
