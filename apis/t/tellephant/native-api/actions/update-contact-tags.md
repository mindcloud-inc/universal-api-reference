# Update contact tags with Tellephant

Updates tags for WhatsApp contacts in Tellephant.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/user/tags/update`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Update contact tags](https://app.tellephant.com/api-documentation#update-tags-for-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of contact tag update objects with contact_id and tags. |
