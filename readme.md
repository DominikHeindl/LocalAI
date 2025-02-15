## What’s included

[**ollama**](https://ollama.com/) - Get up and running with Llama 3.3, DeepSeek-R1, Phi-4, Gemma 2, and other large language models. 

[**open-webui**](https://openwebui.com/) - User-friendly AI Interface (Supports Ollama, OpenAI API, ...) 

[**openedaI**](https://github.com/matatonic/openedai-speech) -  An OpenAI API compatible text to speech server using Coqui AI's xtts_v2 and/or piper tts as the backend.

[**nginx**](https://github.com/nginx/nginx) -  Web Server, high performance Load Balancer, Reverse Proxy, API Gateway and Content Cache.

[**homeassistant**](https://www.postgresql.org/) -  Open source home automation that puts local control and privacy first.


## Install

1. Prerequisites

	-Docker installed
	
	-Nvidia Drivers installed (Optional)

	[**Linux How-to**](https://github.com/DominikHeindl/LocalAI/blob/main/linux_install.md)

2. Download Package
```
git clone https://github.com/DominikHeindl/localAI.git
cd localAI
```

3. Create Self-Signed Certificate or import your own to /ssl
```
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ssl/nginx.key -out ssl/nginx.crt
```

4. Run all Containers
```
docker compose up