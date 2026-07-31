# Get Film by ID with Studio Ghibli

## Endpoint

- **Method:** `GET`
- **Path:** `/films/:id`
- **Base URL:** `https://ghibliapi.vercel.app`
- **Official documentation:** [Get Film by ID](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource UUID documented by the provider. |
| `fields` | query | `string` | no | Optional comma-separated list of response fields documented by the provider. |
