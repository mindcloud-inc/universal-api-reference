# Update Contact with Digiclose

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://app.digiclose.ai/api/v1`
- **Official documentation:** [Update Contact](https://app.digiclose.ai/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | Unique identifier for the contact. |
| `fields` | body | `object` | yes | Contact field values to update. |
