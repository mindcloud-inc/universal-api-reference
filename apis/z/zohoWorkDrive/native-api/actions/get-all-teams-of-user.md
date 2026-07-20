# Get All Teams of User with Zoho WorkDrive

Retrieves teams for a Zoho WorkDrive user.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/users/:zuid/teams`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get All Teams of User](https://workdrive.zoho.com/apidocs/v1/users/getallteamsofuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zuid` | path | `string` | yes | The Zoho user ID whose teams you want to list. |
