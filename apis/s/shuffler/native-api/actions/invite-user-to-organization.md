# Invite User to Organization with Shuffler

Creates an organization invitation in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/register_org`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Invite User to Organization](https://shuffler.io/docs/API#invite-user-to-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | User email to invite. |
