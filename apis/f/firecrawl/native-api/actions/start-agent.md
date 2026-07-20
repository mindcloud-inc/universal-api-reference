# Start Agent with Firecrawl

Creates an agent job in Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Start Agent](https://docs.firecrawl.dev/api-reference/endpoint/agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | no | Optional list of URLs to constrain the agent to |
| `prompt` | body | `string` | yes | The prompt describing what data to extract |
| `schema` | body | `object` | no | Optional JSON schema to structure the extracted data |
| `maxCredits` | body | `number` | no | Maximum credits to spend on this agent task |
| `strictConstrainToURLs` | body | `boolean` | no | Only visit URLs provided in the urls array |
| `model` | body | `string` | no | The model to use for the agent task |
