# List Signals for Call with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List Signals for Call](https://docs.buildbetter.ai/pages/api/graphql-queries#get-call-signals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callId` | body | `string` | yes | Return signals linked to this call ID. |
| `limit` | body | `number` | no | Maximum number of signals to return. |
