# Unarchive Thread with Cirra

Restores an archived Cirra thread by thread ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/cirra/threads/:threadId/archive`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadId` | path | `list` | yes | The thread ID. |
