# Send an invitation to join an organization with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/invitations`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Send an invitation to join an organization](https://xata.io/docs/api-reference/organizations/send-an-invitation-to-join-an-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the user to invite |
| `organizationID` | path | `string` | yes | Unique identifier for a specific organization |
