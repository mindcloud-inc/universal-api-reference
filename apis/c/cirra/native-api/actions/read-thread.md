# Get Thread with Cirra

Retrieves a Cirra thread by thread ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cirra/threads/:threadId`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadId` | path | `list` | yes | The Cirra thread id to read. |
| `advanced` | query | `boolean` | no | When true, include advanced thread fields such as composer settings and thread type. |
