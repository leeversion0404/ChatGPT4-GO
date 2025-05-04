# ```LeeVersion-ChatGPT```

<h1 align="center">Hii...Welcome To The Jungle <img src="https://user-images.githubusercontent.com/1303154/88677602-1635ba80-d120-11ea-84d8-d263ba5fc3c0.gif" width="40px" alt="hi"><br>I'm LeeVersion 😇 </h1>
<p align="center">
  <img src="https://i.ibb.co.com/842LsMKj/1745929182469.jpg" /></>
</p>

- 👼 My name is Ali Ramadhan
- 🗣️ Be Yourself
- 🔭 I am not programmer

# Go-ChatGPT

Go-ChatGPT is an open-source GoLang client for ChatGPT, a large language model trained by OpenAI. With Go-ChatGPT, you can quickly and easily integrate ChatGPT's language processing capabilities into your Go applications.

## Features

- [x] Easy-to-use GoLang client for ChatGPT
- [x] Sends text to ChatGPT and receives a response
- [x] Support custom model and parameters
- [x] Supports GPT4 models 


## Installation

You can install ChatGPT-Go using Go modules:

```bash
go get github.com/leeversion0404/ChatGPT4-GO
```

## Getting Started
Get your API key from the OpenAI Dashboard - [https://platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys) and export this either as an environment variable, or put this your `.bashrc` or `.zshrc`
```bash
export OPENAI_KEY=sk...
```

___

1. In your Go code, import the ChatGPT-Go package:
    ```go
    import (
        "github.com/leeversion0404/ChatGPT4-GO"
    )
    ```

2. Create a new ChatGPT client with your API key
    ```go
    key := os.Getenv("OPENAI_KEY")

    client, err := chatgpt.NewClient(key)
	if err != nil {
		log.Fatal(err)
	}
    ```
3. Use the `SimpleSend` API to send text to ChatGPT and get a response.
   ```go
    ctx := context.Background()
	
    res, err := c.SimpleSend(ctx, "Hello, how are you?")
	if err != nil {
		// handle error
	}
   ```
   The SimpleSend method sends the specified text to ChatGPT and returns a response. If an error occurs, it returns an error message.
4. To use a custom model/parameters, use the `Send` API.
   ```go
    ctx := context.Background()
    
    res, err = c.Send(ctx, &chatgpt.ChatCompletionRequest{
		Model: chatgpt.GPT35Turbo,
		Messages: []chatgpt.ChatMessage{
			{
				Role: chatgpt.ChatGPTModelRoleSystem,
				Content: "Hey, Explain GoLang to me in 2 sentences.",
			},
		},
	})
	if err != nil {
		// handle error
	}
   ```
## Contribute
If you want to contribute to this project, feel free to open a PR or an issue.


## License
This package is licensed under MIT license. See [LICENSE](./LICENSE) for details.


## ```Connect with me```
<p align="center">
  <a href="https://line.me/ti/p/36H-VDctGc"><img src="https://img.shields.io/badge/Line-25D366?style=for-the-badge&logo=line&logoColor=white" />
  <a href="https://github.com/leeversion0404"><img src="https://img.shields.io/badge/-GitHub-black?style=flat-square&logo=github" /> 

</p>
