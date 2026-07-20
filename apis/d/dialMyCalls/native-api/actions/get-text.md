# Get Text with DialMyCalls

Retrieves a text from DialMyCalls.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/text/:TextId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Get Text](https://www.dialmycalls.com/api-documentation#text-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TextId` | path | `string` | yes | The DialMyCalls text ID to retrieve. |
