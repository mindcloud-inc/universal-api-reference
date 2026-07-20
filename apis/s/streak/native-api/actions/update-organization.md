# Update Organization with Streak

Updates an existing organization in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationKey`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Update Organization](https://streak.readme.io/reference/update-an-organization)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationKey` | path | `string` | yes |
| `name` | body | `string` | no |
| `domains` | body | `string` | no |
| `industry` | body | `string` | no |
| `phoneNumbers` | body | `string` | no |
| `addresses` | body | `string` | no |
| `employeeCount` | body | `string` | no |
| `logoURL` | body | `string` | no |
| `other` | body | `string` | no |
| `twitterHandle` | body | `string` | no |
| `facebookHandle` | body | `string` | no |
| `linkedinHandle` | body | `string` | no |
