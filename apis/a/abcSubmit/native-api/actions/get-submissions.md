# Get Submissions with AbcSubmit

Retrieves submissions for an AbcSubmit form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/submissions/:form_id`
- **Base URL:** `https://www.abcsubmit.com`
- **Official documentation:** [Get Submissions](https://www.abcsubmit.com/site/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form whose submissions you want to list. |
| `limit` | query | `number` | no | Optional limit on returned submissions. |
| `skip` | query | `number` | no | Optional number of submissions to skip. |
