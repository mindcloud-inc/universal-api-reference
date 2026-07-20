# List Feedback with LangChain

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/feedback`
- **Base URL:** `https://api.smith.langchain.com`
- **Official documentation:** [List Feedback](https://api.smith.langchain.com/redoc#tag/feedback/operation/read_feedbacks_api_v1_feedback_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run` | query | `string` | no | Filter feedback by run id. |
| `session` | query | `string` | no | Filter feedback by session id. |
| `key` | query | `string` | no | Filter feedback by key. |
