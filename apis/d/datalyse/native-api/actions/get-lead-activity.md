# Get Lead Activity with Datalyse

Retrieves activity for a contact from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/leads/getactivity.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Get Lead Activity](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | body | `string` | yes | ID of the contact |
| `type` | body | `string` | no | Filter by activity type: callin, callout, email, emailin, emailout, note, sms, form_completed, etc. (optional) |
| `var_page` | body | `string` | no | Page number |
| `var_resultspage` | body | `string` | no | Maximum number of results to display |
