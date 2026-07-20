# List Sessions with LangChain

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/sessions`
- **Base URL:** `https://api.smith.langchain.com`
- **Official documentation:** [List Sessions](https://api.smith.langchain.com/redoc#tag/tracer-sessions/operation/read_tracer_sessions_api_v1_sessions_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of sessions to return. |
| `offset` | query | `number` | no | Number of sessions to skip. |
| `name` | query | `string` | no | Filter sessions by name. |
