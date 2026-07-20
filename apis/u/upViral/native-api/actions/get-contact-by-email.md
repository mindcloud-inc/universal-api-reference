# Get Contact By Email with UpViral

Retrieves a campaign contact from UpViral by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://app.upviral.com/api/v1/`
- **Official documentation:** [Get Contact By Email](https://www.upviral.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The UpViral campaign ID containing the contact. |
| `email` | body | `string` | yes | The contact email address. |
