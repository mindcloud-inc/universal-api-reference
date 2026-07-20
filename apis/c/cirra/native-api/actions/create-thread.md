# Create Thread with Cirra

Creates a Cirra thread and starts its initial run.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/cirra/threads`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The first user message to add to the new thread. |
