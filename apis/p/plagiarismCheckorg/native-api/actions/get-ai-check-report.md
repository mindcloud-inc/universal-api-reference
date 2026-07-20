# Get AI Check Report with PlagiarismCheck.org

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/chat-gpt/:id`
- **Base URL:** `https://plagiarismcheck.org`
- **Official documentation:** [Get AI Check Report](https://plagiarismcheck.org/for-developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | AI check identifier returned by Submit AI Check From Text or Submit AI Check From File. |
