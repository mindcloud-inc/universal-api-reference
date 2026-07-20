# Delete Authentication Codes with Porsline

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/surveys/:survey_id/settings/authentication-codes/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Delete Authentication Codes](https://developers.porsline.com/#tag/Authentication-codes/paths/~1api~1surveys~1{survey_id}~1settings~1authentication-codes~1/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `codes` | body | `list<string>` | no | Authentication codes to delete. |
