# Create Invitation with Documently

Creates a new invitation in Documently.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Create Invitation](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/ld+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Invitee email. |
| `firstname` | body | `string` | no | Invitee first name. |
| `lastname` | body | `string` | no | Invitee last name. |
| `organization` | body | `string` | no | Organization IRI. |
| `project` | body | `string` | no | Project IRI. |
| `role` | body | `string` | no | Invitation role. |
| `status` | body | `string` | no | Invitation status. |
