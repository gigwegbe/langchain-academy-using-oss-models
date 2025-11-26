## INFERENCE ENGINES 
  
### Ollama Setup
To be honest, ollama is the simplest inference engine, so we would start with that. Just make sure you have the Ollama setup installed on your machine. Check the link for the installation - [Link](https://ollama.com/)

- Download the model by running the command below: 
```
ollama run gpt-oss:20b
```

### GGT-OSS Thinking Level ["low","medium","high"]
```
llm = ChatOllama(
    model="gpt-oss:20b",
    validate_model_on_init=True,
    temperature=0,
    model_kwargs={"think": "high"}
)
```
