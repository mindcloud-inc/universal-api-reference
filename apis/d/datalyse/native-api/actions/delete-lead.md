# Delete Lead with Datalyse

Deletes an existing contact or company from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/leads/delete.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Delete Lead](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | body | `string` | yes | ID of the contact or company to delete |
