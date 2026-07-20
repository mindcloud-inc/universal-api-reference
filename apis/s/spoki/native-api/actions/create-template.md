# Create Template with Spoki

Creates a WhatsApp template for the authenticated account or a specific active WhatsApp channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Create Template](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | yes | Template fields to create, using Spoki's template schema. |
