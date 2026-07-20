# Update api token with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/api-tokens/{id}/update`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update api token](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `name` | body | `string` | yes | Name for api token |
