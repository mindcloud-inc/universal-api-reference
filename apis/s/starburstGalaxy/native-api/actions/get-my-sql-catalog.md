# Get MySQL catalog with Starburst Galaxy

## Endpoint

- **Method:** `GET`
- **Path:** `/public/api/v1/catalogType/mysql/catalog/{catalogId}`
- **Base URL:** `https://mindcloud.galaxy.starburst.io`
- **Official documentation:** [Get MySQL catalog](https://galaxy.starburst.io/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `catalogId` | path | `string` | yes | Starburst Galaxy catalog ID. Docs also support URL-encoded lookup expressions such as name=value. |
