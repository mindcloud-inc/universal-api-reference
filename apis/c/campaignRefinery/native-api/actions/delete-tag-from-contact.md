# Delete Tag from Contact with Campaign Refinery

Deletes a tag from a contact in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/delete-tag`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Delete Tag from Contact](https://developers.campaignrefinery.com/reference/delete-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The contact's ID. |
| `tag_id` | body | `string` | yes | The tag UUID. |
