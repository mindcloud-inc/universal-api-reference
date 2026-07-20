# List Case Messages with Sprinklr

Retrieves case messages from Sprinklr.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v2/case/associated-messages`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Case Messages](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcase%2Fassociated-messages/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `epoch_time` | query | `number` | no |
| `id` | query | `string` | yes |
