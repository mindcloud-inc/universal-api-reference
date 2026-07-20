# Assign BPM Role with Agilite

Assigns a role to a BPM record in Agilite.

## Endpoint

- **Method:** `GET`
- **Path:** `/bpm/assignRole`
- **Base URL:** `https://api.agilite.io`
- **Official documentation:** [Assign BPM Role](https://docs.agilite.io/reference/assignrole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bpm-record-id` | query | `string` | yes | BPM record identifier. |
| `current-user` | query | `string` | yes | Name, email, or ID of the user assigning the BPM role. |
| `role-name` | query | `string` | yes | BPM role to assign. |
| `responsible-users` | query | `string` | yes | Users responsible for the role assignment. |
