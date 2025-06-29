# ollama

if running Ollama on windows and looking for remote access, then ensure that a system variable is added to as follows:

key OLLAMA_HOST 
value 0.0.0.0:11434


example of a remote commands to 192.168.68.127

curl http://192.168.68.127:11434/api/generate -d '{
  "model": "mistral",
  "prompt": "Why is the sky blue?",
  "stream": false
}'  | jq -r '.response'




#to install Qwen3 on 32B:

ollama pull qwen3:32b-q8_0
or
ollama pull qwen2.5-coder:32b

or look for any model under: https://ollama.com/library/ 


