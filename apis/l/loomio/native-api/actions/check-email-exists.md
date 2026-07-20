# Check Email Exists with Loomio

Checks whether an email exists in Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/profile/email_exists`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [Check Email Exists](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/profile_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | The email address to check. |
