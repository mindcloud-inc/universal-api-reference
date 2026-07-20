# Create Highlights with Glasp

Creates new highlights in your Glasp account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/highlights/create`
- **Base URL:** `https://api.glasp.co`
- **Official documentation:** [Create Highlights](https://glasp.co/docs/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlights[]` | body | `array<object>` | yes | Array of Glasp highlight objects to create. Each object should include at least title, url, and text. |
