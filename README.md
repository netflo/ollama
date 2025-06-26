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
