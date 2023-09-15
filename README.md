# Open Interpreter Container

[Open Interpreter](https://github.com/KillianLucas/open-interpreter) on Docker Container.

- Using Docker Compose.


## Usage

- Create environment variables.

`.env`
```
INTERPRETER_CLI_AUTO_RUN=False
INTERPRETER_CLI_FAST_MODE=False
INTERPRETER_CLI_LOCAL_RUN=False
INTERPRETER_CLI_DEBUG=False
OPENAI_API_KEY=YOUR_OPEN_AI_API_KEY
```


## Build Image

```bash
docker compose build
```

## Run Container

```bash
docker compose run --rm interpreter /bin/bash
```

## Open Interpreter

### with CLI
```bash
root@xxxxxxxxxxxx:/app# interpreter
```

```
▌ Model set to GPT-4 
Tip: To run locally, use interpreter --local                                               
Open Interpreter will require approval before running code. Use interpreter -y to bypass this.                                                     
Press CTRL-C to exit.                                                 
```

```
> 何が出来るの？
                                       
  私はプログラミングの専門家で、あなたが目指す目標を達成するために必要なコードを実行することができます。具体的には、以下のようなことが可能です：   
                                       
   1 データ分析：PythonやRを使ってデータを分析し、結果を視覚化します。                                                                             
   2 ファイル操作：ファイルの作成、....
```


### with Python

`./app/main.py`

```python

import interpreter

interpreter.chat("何が出来るの？")

# Starting Chat
interpreter.chat()

```

Execute

```bash
root@xxxxxxxxxxxx:/app# python3 main.py
```

