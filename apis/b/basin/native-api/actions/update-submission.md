# Update Submission with Basin

Updates an existing submission in Basin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/submissions/:id`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [Update Submission](https://usebasin.com/api_docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the submission to update. |
| `submission` | body | `object` | no | Submission fields to update. |
| `submission.spam` | body | `boolean` | no | Set whether the submission is marked as spam. |
| `submission.read` | body | `boolean` | no | Set whether the submission is marked as read. |
| `submission.trash` | body | `boolean` | no | Set whether the submission is moved to trash. |
