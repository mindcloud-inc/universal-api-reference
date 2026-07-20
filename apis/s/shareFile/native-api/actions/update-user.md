# Update User with ShareFile

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Users({{id}})`
- **Base URL:** `https://{subdomain}.{apicp}/sf/v3`
- **Official documentation:** [Update User](https://api.sharefile.com/html/docs/Users.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ShareFile user identifier to update. |
| `Email` | body | `string` | no | The email address for the ShareFile user. |
| `FirstName` | body | `string` | no | The first name of the ShareFile user. |
| `LastName` | body | `string` | no | The last name of the ShareFile user. |
| `Company` | body | `string` | no | The company name for the ShareFile user. |
