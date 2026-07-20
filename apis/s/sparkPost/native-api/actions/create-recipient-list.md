# Create Recipient List with SparkPost

## Endpoint

- **Method:** `POST`
- **Path:** `/recipient-lists`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Create Recipient List](https://developers.sparkpost.com/api/recipient-lists/#recipient-lists-post-create-a-recipient-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Unique recipient list identifier. |
| `name` | body | `string` | no | Human-readable recipient list name. |
| `recipients[]` | body | `array<object>` | yes | Recipients included in the stored list. |
