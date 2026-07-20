# Create Attribute with Campaign Refinery

Creates a new attribute in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/attributes/create-attribute`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Create Attribute](https://developers.campaignrefinery.com/reference/create-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The attribute's name. |
| `group` | body | `string` | yes | The group UUID. |
| `type` | body | `string` | yes | Attribute type: int, decimal, varchar, datetime, or mediumtext. |
