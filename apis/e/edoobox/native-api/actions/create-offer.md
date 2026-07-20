# Create Offer with Edoobox

Creates a new offer in Edoobox.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Create Offer](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | Parent edoobox category ID for the new offer. |
| `name` | body | `string` | yes | Display name for the new offer. |
| `number` | body | `string` | yes | Unique offer number/code. |
| `type` | body | `string` | yes | edoobox offer type. Defaults to offer. |
