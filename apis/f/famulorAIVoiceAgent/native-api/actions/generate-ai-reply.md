# Generate AI Reply with Famulor AI - Voice Agent

Generates an AI reply in Famulor by customer identifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-replies/generate`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Generate AI Reply](https://docs.famulor.io/en/api-reference/ai-replies/generate-reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Message or prompt to generate a reply for. |
