# Get Submissions Count with AbcSubmit

Retrieves the submission count for an AbcSubmit form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/submissions/:form_id/count`
- **Base URL:** `https://www.abcsubmit.com`
- **Official documentation:** [Get Submissions Count](https://www.abcsubmit.com/site/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form whose submission count you want. |
