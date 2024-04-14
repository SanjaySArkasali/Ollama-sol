# Ollama-sol

No Worries Guys Got it,

Here  is the solution ,
Upon going through docs, first we need to run ollama server by setting the host port and the allowed origins to communicate with it,

Run
```bash
export OLLAMA_HOST="0.0.0.0:8888" OLLAMA_ORIGINS="*" ollama serve
```
"*" for all if you want to use particular ip use "http:// or https://" followed by the ip you want to allow

then start the ollama serve by

```bash
ollama serve
```
then run the api such as 
```bash
curl http://<pub-ip>:8888/api/pull -d '{
  "name": "llama2"
}'
```
to pull and image only once is enough (you can pull your desired model)

and
 
```bash
curl http://<pub-ip>:8888/api/generate -d '{
  "model": "llama2",
  "prompt":"Why is the sky blue?",
  "response": "The",
  "done": false
}'
```
