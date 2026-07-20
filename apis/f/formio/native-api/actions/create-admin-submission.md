# Create Admin Submission with Form.io

Creates a new admin submission in your Form.io project.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/submission`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Create Admin Submission](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.email` | body | `string` | yes | Email stored on the admin submission. |
| `data.password` | body | `string` | yes | Password stored on the admin submission. |
