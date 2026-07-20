# Get Contact with UpViral

Retrieves a campaign contact from UpViral.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://app.upviral.com/api/v1/`
- **Official documentation:** [Get Contact](https://www.upviral.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The UpViral campaign ID containing the contact. |
| `lead_id` | body | `string` | yes | The contact's UpViral lead ID. |
