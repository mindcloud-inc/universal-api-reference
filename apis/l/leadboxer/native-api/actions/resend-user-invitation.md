# Resend User Invitation with Leadboxer

Resends a user invitation in Leadboxer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/{{userId}}/invite/resend`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Resend User Invitation](https://developers.leadboxer.com/reference/resendinvite)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | path | `number` | yes |
| `email` | query | `string` | yes |
