# Create Campaign with Tremendous

Creates a new campaign in Tremendous.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://testflight.tremendous.com/api/v2`
- **Official documentation:** [Create Campaign](https://developers.tremendous.com/reference/create-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Description of the campaign |
| `name` | body | `string` | yes | Name of the campaign |
| `products[]` | body | `array<string>` | yes | Product IDs available in the campaign |
