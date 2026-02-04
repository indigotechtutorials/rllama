# Todo list

I want to make this CLI even better

### Support passing in a raw hugging face url like 

Pass a url for any hugging face model
https://huggingface.co/hugging-quants/Llama-3.2-1B-Instruct-Q8_0-GGUF

extract the org name, repo and filename to construct a huggingface downloadable url like this.

The org and repo are the first two params in the url org: `hugging-quants` repo: `Llama-3.2-1B-Instruct-Q8_0-GGUF`

Hugging face has an API you can use to get metadata about an orgname/repo use this to look for a file to download.

`curl https://huggingface.co/api/models/bartowski/Llama-3.2-1B-Instruct-GGUF`

The API docs are here https://huggingface.co/spaces/huggingface/openapi
but they are pretty bad they don't even reference the route we need for this call. ^^

click on Files & Versions and look for a file with the extension .gguf

`<org>/<repo>/<filename>`