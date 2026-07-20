# Add Form to Contact with Campaign Refinery

Adds a form to a contact in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/add-form`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Add Form to Contact](https://developers.campaignrefinery.com/reference/add-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The contact's ID. |
| `form_id` | body | `string` | yes | The form UUID. |
