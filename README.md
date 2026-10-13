# switch-trust-demo

A test repository for the
[Switch Trust Inventory Scan](https://github.com/sandbox-quantum/switch-trust-codescan-action)
GitHub Action. The action statically analyzes a repository for AI assets such as
models, agents and MCP servers, and sends the resulting inventory to a
[Switch Trust](https://www.switchagents.ai/) instance.

## What's here

- [`examples/`](examples/) holds small AI applications for the scanner to find:
  a Google ADK agent and a Gemma text-generation pipeline.
- [`.github/workflows/switch-trust-codescan-action.yml`](.github/workflows/switch-trust-codescan-action.yml)
  runs the action every weekday and on demand.

## Running it in your own repository

Add two repository secrets:

| Secret | Value |
| ------ | ----- |
| `SWITCH_TRUST_TOKEN` | API key for your Switch Trust instance |
| `LLM_API_KEY` | API key for the provider named in `llm_model` |

Then copy the workflow and point `switch_trust_instance` at your instance. See the
[action's README](https://github.com/sandbox-quantum/switch-trust-codescan-action#readme)
for every input.

## License

[Apache-2.0](LICENSE)
