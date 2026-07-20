# Ask Express Agent with You.com

Retrieves an express agent response from You.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/runs`
- **Base URL:** `https://api.you.com`
- **Official documentation:** [Ask Express Agent](https://docs.you.com/custom-solutions/agents/express-agent/express-agent-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Question to answer. |
