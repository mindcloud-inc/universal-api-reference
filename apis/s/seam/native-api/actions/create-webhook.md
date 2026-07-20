# Create Webhook with Seam

Creates a new webhook in Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/create`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [Create Webhook](https://docs.seam.co/latest/api/webhooks/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_types` | body | `list<string>` | no |
| `url` | body | `string` | yes |
