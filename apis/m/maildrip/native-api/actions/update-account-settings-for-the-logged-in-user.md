# Update account settings for the logged-in user with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/users/account-settings`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Update account settings for the logged-in user](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phoneNumber` | body | `string` | no |
| `companyName` | body | `string` | no |
| `website` | body | `string` | no |
| `city` | body | `string` | no |
| `state` | body | `string` | no |
| `officeAddress` | body | `string` | no |
| `language` | body | `string` | no |
| `email` | body | `string` | no |
| `fullname` | body | `string` | no |
