# Create Tags with lc.cx

Creates one or more tags in lc.cx.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/create`
- **Base URL:** `https://api.lc.cx/v1`
- **Official documentation:** [Create Tags](https://dev.lc.cx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<object>` | yes | An array of tag objects to create, each with a name and optional color. |
