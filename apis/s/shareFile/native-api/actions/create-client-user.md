# Create Client User with ShareFile

## Endpoint

- **Method:** `POST`
- **Path:** `/Users`
- **Base URL:** `https://{subdomain}.{apicp}/sf/v3`
- **Official documentation:** [Create Client User](https://api.sharefile.com/html/docs/Users.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | The email address for the ShareFile user. |
| `FirstName` | body | `string` | yes | The first name of the ShareFile user. |
| `LastName` | body | `string` | yes | The last name of the ShareFile user. |
| `Company` | body | `string` | yes | The company name for the ShareFile user. |
