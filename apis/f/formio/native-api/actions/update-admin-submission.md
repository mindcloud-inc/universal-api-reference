# Update Admin Submission with Form.io

Updates an existing admin submission in your Form.io project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/submission/:submissionId`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Update Admin Submission](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.email` | body | `string` | no | Updated email stored on the admin submission. |
| `data.password` | body | `string` | no | Updated password stored on the admin submission. |
| `submissionId` | path | `string` | yes | The submission ID. |
