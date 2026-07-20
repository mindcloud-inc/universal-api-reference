# Create User with SweetProcess

Creates a new teammate in SweetProcess.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/`
- **Base URL:** `https://www.sweetprocess.com/api/v1`
- **Official documentation:** [Create User](https://www.sweetprocess.com/kb/8LBTequD/article/L4CaqHMav/interim-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The teammate's display name. |
| `email` | body | `string` | yes | The teammate's email address. |
| `is_super_manager` | body | `boolean` | no | Whether the new teammate should be invited as a super manager. |
