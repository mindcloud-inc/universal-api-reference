# Add Contact Points with UpViral

Updates a contact's points in UpViral.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://app.upviral.com/api/v1/`
- **Official documentation:** [Add Contact Points](https://www.upviral.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The UpViral campaign ID containing the contact. |
| `lead_id` | body | `string` | yes | The contact's UpViral lead ID. |
| `points` | body | `number` | yes | Number of points to add to the contact. |
