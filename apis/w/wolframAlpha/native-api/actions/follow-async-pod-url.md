# Follow Async Pod URL with Wolfram Alpha

Retrieves an asynchronous pod result from Wolfram Alpha.

## Endpoint

- **Method:** `GET`
- **Path:** `{{asyncPodUrl}}`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Follow Async Pod URL](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asyncPodUrl` | query | `string` | yes | Full async pod URL returned by a prior Full Results response. |
