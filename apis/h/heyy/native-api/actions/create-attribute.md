# Create Attribute with Heyy

Creates a new attribute in Heyy.

## Endpoint

- **Method:** `POST`
- **Path:** `/attributes`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Create Attribute](https://docs.heyy.io/api-reference/create-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional attribute description. |
| `externalId` | body | `string` | yes | The stable external ID for the attribute. |
| `name` | body | `string` | yes | The attribute display name. |
