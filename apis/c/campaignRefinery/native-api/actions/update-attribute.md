# Update Attribute with Campaign Refinery

Updates an existing attribute in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/attributes/update-attribute`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Update Attribute](https://developers.campaignrefinery.com/reference/update-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The attribute UUID. |
| `name` | body | `string` | no | The attribute's name. |
| `group` | body | `string` | no | The group UUID. |
