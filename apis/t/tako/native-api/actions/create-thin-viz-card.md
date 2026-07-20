# Create Thin-Viz Card with Tako

Creates an embeddable Thin-Viz card in Tako.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/thin_viz/create/`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Create Thin-Viz Card](https://docs.tako.com/api-reference/thinviz-direct-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `components[]` | body | `array<object>` | yes | Array of Thin-Viz component configurations that define the card layout and data. |
