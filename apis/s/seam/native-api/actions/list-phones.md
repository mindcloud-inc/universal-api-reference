# List Phones with Seam

Retrieves a list of phones from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/phones/list`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [List Phones](https://docs.seam.co/latest/api/phones/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acs_credential_id` | body | `string` | no | ID of the credential by which you want to filter phones. |
| `owner_user_identity_id` | body | `string` | no | ID of the owner user identity by which you want to filter phones. |
