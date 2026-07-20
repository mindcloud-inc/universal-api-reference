# Create Authentication Codes with Porsline

## Endpoint

- **Method:** `POST`
- **Path:** `/api/surveys/:survey_id/settings/authentication-codes/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Create Authentication Codes](https://developers.porsline.com/#tag/Authentication-codes/paths/~1api~1surveys~1{survey_id}~1settings~1authentication-codes~1/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `codes` | body | `list<string>` | yes | List of authentication code strings to create. |
