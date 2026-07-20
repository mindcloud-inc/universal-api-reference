# Update changelogs with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/product-versions/{id}/update-changelog`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update changelogs](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `changelog` | body | `string` | no | New changelog |
