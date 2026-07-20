# Update firmware changelog with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmware-changelogs/{id}/update`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update firmware changelog](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `changelog` | body | `string` | no | Changelog for firmware |
