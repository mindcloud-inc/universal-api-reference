# List Survey Authentication Codes with Porsline

## Endpoint

- **Method:** `GET`
- **Path:** `/api/surveys/:survey_id/settings/authentication-codes/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [List Survey Authentication Codes](https://developers.porsline.com/#tag/Authentication-codes/paths/~1api~1surveys~1{survey_id}~1settings~1authentication-codes~1/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `page` | query | `number` | no | Page number. |
| `page_size` | query | `number` | no | Maximum number of authentication codes to return. |
