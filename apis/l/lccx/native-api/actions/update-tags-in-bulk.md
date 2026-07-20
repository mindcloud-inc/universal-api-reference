# Update Tags in Bulk with lc.cx

Updates tags in bulk in lc.cx.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/update/bulk`
- **Base URL:** `https://api.lc.cx/v1`
- **Official documentation:** [Update Tags in Bulk](https://dev.lc.cx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<object>` | yes | An array of tag objects to update, each with id, name, and optional color. |
