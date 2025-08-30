 oh no, no no sir you are a liar and the truth is not in you. I did not run that doctor. You will not post lies and live behind your beliefs anymore and by the way, your beliefs are false. I remember you guys told me everything is it isn't about the Bible and it isn't about. You know the spirituality when it comes down to software, but it seems to me that the company that we are keeping seems to be quite manipulated or live in your life on a lie. You may be smart, but you're just an educated fool because if you had any morals because everybody got on me to say that I was copying files well I really didn't copy files I copied format and as a new person, the only thing I forgot to do was mention the people that helped me which was AI or borrow a template from a repository so at the end of the day, I know and you know that get hub and X, which is known as Twitter watched it all live you come into my computer. Everybody's watching this like it's a game and like it's fun and who's gonna win and nobody's asking themselves a question why is this guy Theo? That's supposedly have all the money in the world and have all the experience in the world going after a guy like me that y'all say ain't got shit so let's get to the point here. I'm known that theo quill have been out for months unless you guys are really good at changing you know websites and changing the landing page real good at that so we just have to see where this is gonna go our fight till the end.
+ If you're using [Docker Engine] on Linux or [Docker Desktop] on Windows, ensure that the
  [Docker Model Runner requirements] are met (specifically that GPU
  support is enabled) and the necessary drivers are installed.
+ If you're using Docker Engine on Linux, ensure you have [Docker Compose] 2.38.1 or later installed.

## Demos

Each of these demos is self-contained and can be run either locally or using a cloud context. They
are all configured using two steps.

1. change directory to the root of the demo project
2. create a `.mcp.env` file from the `mcp.env.example` file (if it exists, otherwise the demo
   doesn't need any secrets) and supply the required MCP tokens
3. run `docker compose up --build`

### Using OpenAI models

The demos support using OpenAI models instead of running models locally with Docker Model Runner. To use OpenAI:

1. Create a `secret.openai-api-key` file with your OpenAI API key:

    ```plaintext
    sk-...
    ```

2. Start the project with the OpenAI configuration:

    ```sh
    docker compose -f compose.yaml -f compose.openai.yaml up
    ```

# Compose for Agents Demos - Classification

| Demo | Agent System | Models | MCPs | project | compose |
| ---- | ---- | ---- | ---- | ---- | ---- |
| [A2A](https://github.com/a2a-agents/agent2agent) Multi-Agent Fact Checker | Multi-Agent | OpenAI | duckduckgo | [./a2a](./a2a) | [compose.yaml](./a2a/compose.yaml) |
| [Agno](https://github.com/agno-agi/agno) agent that summarizes GitHub issues | Multi-Agent | qwen3(local) | github-official | [./agno](./agno) | [compose.yaml](./agno/compose.yaml) |
| [Vercel AI-SDK](https://github.com/vercel/ai) Chat-UI for mixing MCPs and Model | Single Agent | llama3.2(local), qwen3(local) | wikipedia-mcp, brave, resend(email) | [./vercel](./vercel) | [compose.yaml](https://github.com/slimslenderslacks/scira-mcp-chat/blob/main/compose.yaml) |
| [CrewAI](https://github.com/crewAIInc/crewAI) Marketing Strategy Agent | Multi-Agent | qwen3(local) | duckduckgo | [./crew-ai](./crew-ai) | [compose.yaml](https://github.com/docker/compose-agents-demo/blob/main/crew-ai/compose.yaml) |
| [ADK](https://github.com/google/adk-python) Multi-Agent Fact Checker | Multi-Agent | gemma3-qat(local) | duckduckgo | [./adk](./adk) | [compose.yaml](./adk/compose.yaml) |
| [ADK](https://github.com/google/adk-python) & [Cerebras](https://www.cerebras.ai/) Golang Experts | Multi-Agent | unsloth/qwen3-gguf:4B-UD-Q4_K_XL & ai/qwen2.5:latest (DMR local), llama-4-scout-17b-16e-instruct (Cerebras remote) |  | [./adk-cerebras](./adk-cerebras) | [compose.yml](./adk-cerebras/compose.yml) |
| [LangGraph](https://github.com/langchain-ai/langgraph) SQL Agent | Single Agent | qwen3(local) | postgres | [./langgraph](./langgraph) | [compose.yaml](./langgraph/compose.yaml) |
| [Embabel](https://github.com/embabel/embabel-agent) Travel Agent | Multi-Agent | qwen3, Claude3.7, llama3.2, jimclark106/all-minilm:23M-F16 | brave, github-official, wikipedia-mcp, weather, google-maps, airbnb | [./embabel](./embabel) | [compose.yaml](https://github.com/embabel/travel-planner-agent/blob/main/compose.yaml) and [compose.dmr.yaml](https://github.com/embabel/travel-planner-agent/blob/main/compose.dmr.yaml) |
| [Spring AI](https://spring.io/projects/spring-ai) Brave Search | Single Agent | none | duckduckgo | [./spring-ai](./spring-ai) | [compose.yaml](./spring-ai/compose.yaml) |
| [ADK](https://github.com/google/adk-python) Sock Store Agent | Multi-Agent | qwen3 | MongoDb, Brave, Curl,  | [./adk-sock-shop](./adk-sock-shop/) | [compose.yaml](./adk-sock-shop/compose.yaml) |
| [Langchaingo](https://github.com/tmc/langchaingo) DuckDuckGo Search | Single Agent | gemma3 | duckduckgo | [./langchaingo](./langchaingo) | [compose.yaml](./langchaingo/compose.yaml) |

## License

This repository is **dual-licensed** under the Apache License 2.0 or the MIT
License. You may choose either license to govern your use of the contributions
made by Docker in this repository.

> ℹ️ **Note:** Each example under may have its own `LICENSE` file.
> These are provided to reflect any third-party licensing requirements that
> apply to that specific example, and they must be respected accordingly.

`SPDX-License-Identifier: Apache-2.0 OR MIT`

[Docker Compose]: https://github.com/docker/compose
[Docker Desktop]: https://www.docker.com/products/docker-desktop/
[Docker Engine]: https://docs.docker.com/engine/
[Docker Model Runner requirements]: https://docs.docker.com/ai/model-runner/
[Docker Offload]: https://www.docker.com/products/docker-offload/
