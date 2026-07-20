# Create Multiple Links with Linkbreakers

Creates multiple new links in Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links/bulk`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Create Multiple Links](https://linkbreakers.com/help/api/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `links[]` | body | `array<object>` | yes | Links to create in one batch. |
