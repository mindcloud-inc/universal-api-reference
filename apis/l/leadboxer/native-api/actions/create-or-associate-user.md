# Create Or Associate User with Leadboxer

Creates a user in Leadboxer, or associates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Create Or Associate User](https://developers.leadboxer.com/reference/adduser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `email` | body | `string` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
| `accountId` | body | `string` | yes |
| `timezone` | body | `string` | yes |
| `datasetIds[]` | body | `array<string>` | yes |
| `sendEmail` | body | `boolean` | no |
