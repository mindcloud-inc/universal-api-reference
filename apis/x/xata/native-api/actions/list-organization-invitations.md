# List invitations for an organization with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/invitations`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [List invitations for an organization](https://xata.io/docs/api-reference/organizations/list-invitations-for-an-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter invitations by status |
| `email` | query | `string` | no | Filter invitations by email address |
| `first_name` | query | `string` | no | Filter invitations by first name |
| `last_name` | query | `string` | no | Filter invitations by last name |
| `search` | query | `string` | no | Search invitations by email or name |
| `first` | query | `number` | no | Index of the first result to return (0-based offset for pagination) |
| `max` | query | `number` | no | Maximum number of results to return |
| `organizationID` | path | `string` | yes | Unique identifier for a specific organization |
