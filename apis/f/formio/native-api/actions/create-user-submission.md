# Create User Submission with Form.io

Creates a new user submission in your Form.io project.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/submission`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Create User Submission](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.email` | body | `string` | yes | Email stored on the user submission. |
| `data.password` | body | `string` | yes | Password stored on the user submission. |
