# Add Tag to Contact with Campaign Refinery

Adds a tag to a contact in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/add-tag`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Add Tag to Contact](https://developers.campaignrefinery.com/reference/add-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The contact's ID. |
| `tag_id` | body | `string` | no | The tag UUID. |
| `tag_ids` | body | `string` | no | One or more tag UUIDs. Send multiple values as a string separated by `,`. |
