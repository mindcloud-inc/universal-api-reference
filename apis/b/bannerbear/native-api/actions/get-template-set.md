# Get Template Set with Bannerbear

Retrieves template set from Bannerbear.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/template_sets/:uid`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Get Template Set](https://developers.bannerbear.com/v2/#retrieve-a-template-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The unique ID of the template set to retrieve. |
| `extended` | query | `boolean` | no | Return the extended response including current layer defaults. |
