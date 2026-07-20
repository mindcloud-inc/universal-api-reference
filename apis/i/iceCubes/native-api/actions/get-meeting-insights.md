# Get Meeting Insights with IceCubes

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:id/insights`
- **Base URL:** `https://icecubes.app/api/public`
- **Official documentation:** [Get Meeting Insights](https://icecubes.app/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The meeting ID to retrieve insights for. |
| `category` | query | `string` | no | Filter insights by category. |
