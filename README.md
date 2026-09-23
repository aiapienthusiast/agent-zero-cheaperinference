# Cheaper Inference Provider for Agent Zero

Adds [Cheaper Inference](https://cheaperinference.com) as a chat provider in Agent Zero.

Cheaper Inference is an OpenAI-compatible gateway.
It serves models from OpenAI, Anthropic, Google, DeepSeek, Z.ai and other labs, below the list price of each lab.

## Install

Install the plugin from the Agent Zero plugin index.

To install it manually:

```bash
git clone https://github.com/aiapienthusiast/agent-zero-cheaperinference.git usr/plugins/cheaperinference_provider
```

## Set the API key

1. Create an API key at [cheaperinference.com](https://cheaperinference.com/docs#api-keys). Keys start with `ci_live_`.
2. Add funds to your wallet. Billing is prepaid. An empty wallet causes HTTP 402 errors.
3. Enter the key in Agent Zero, or set it in `.env`:

```bash
API_KEY_CHEAPERINFERENCE=ci_live_...
```

## Use

Go to **Settings → Model Configuration → Chat Provider** and select **Cheaper Inference**.
Then select a model, for example `gpt-5.4` or `claude-opus-5`.

The model picker loads the current list from `GET https://api.cheaperinference.com/v1/models`.

## Limits

- The list also contains image and video models. They do not work in chat.
- The gateway has no embeddings endpoint. Use another provider for embeddings.

## License

MIT
