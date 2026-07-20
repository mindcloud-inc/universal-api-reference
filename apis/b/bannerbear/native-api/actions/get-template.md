# Get Template with Bannerbear

Retrieves template from Bannerbear.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/templates/:uid`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Get Template](https://developers.bannerbear.com/v2/#retrieve-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The unique ID of the template to retrieve. |
| `extended` | query | `boolean` | no | Return the extended template response including current layer defaults. |
