# What It Does

This is a fork of https://github.com/joselcaguilar/azure-openai-ha

This is equivalent to the built-in [OpenAI Conversation integration](https://www.home-assistant.io/integrations/openai_conversation/). The difference is that you can use a custom base url.

## Using with HACLIProxyAPI

This integration works great with [HACLIProxyAPI](https://github.com/c128128/HACLIProxyAPI) - a Home Assistant add-on that provides a unified API endpoint for AI services (OpenAI, Claude, Gemini, etc.) using your existing subscriptions.

### Prerequisites

Follow [HACLIProxyAPI setup instructions](https://github.com/c128128/HACLIProxyAPI) (Steps 1-4) to install and configure the proxy add-on first.

### Installation

1. Install this integration via HACS:

   [![image](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=c128128&repository=openai-ha&category=integration)

2. Restart Home Assistant.

3. Go to **Settings** → **Devices & Services** → **Add Integration**.

4. Search for **OpenAI Conversation** and add it.

5. Configure the integration:
   - **API Base URL**: `http://homeassistant.local:8787/v1`
     (or `http://localhost:8787/v1` if running in Docker)
   - **API Key**: Enter any value (e.g., `sk-placeholder`) - the proxy handles authentication

6. Uncheck **Recommended model settings** and set a custom **Model** name. You can check available models at: `http://homeassistant.local:8787/v1/models`

7. Go to **Settings** → **Voice Assistants** and create or edit an assistant to use the new OpenAI conversation agent.

## Support

- [Report Issues](https://github.com/c128128/openai-ha/issues)
- [HACLIProxyAPI](https://github.com/c128128/HACLIProxyAPI)
