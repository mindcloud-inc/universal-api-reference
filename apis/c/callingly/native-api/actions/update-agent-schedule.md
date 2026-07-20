# Update Agent Schedule with Callingly

Updates an agent schedule in Callingly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/agents/{{id}}/schedule`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Update Agent Schedule](https://help.callingly.com/article/38-callingly-api-documentation#update-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `scheduleJson` | body | `string` | yes | Pass the full schedule array as JSON using the Get Agent Schedule response shape. |
