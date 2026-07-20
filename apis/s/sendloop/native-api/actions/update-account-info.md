# Update Account Info with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/account.info.update/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Update Account Info](https://chmyos.notion.site/Update-Account-Info-d83e5542ee4147ec9e27dd95a1bad17e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CompanyName` | body | `string` | no | Name of the account owner company |
| `Email` | body | `string` | no | Email address of the account owner |
| `FirstName` | body | `string` | no | First name of the account owner |
| `LastName` | body | `string` | no | Last name of the account owner |
| `TimeZone` | body | `string` | no | Time zone of the account owner |
| `Username` | body | `string` | no | Username for the Sendloop account |
