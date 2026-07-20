# Create Badge List with Ubiqod by Skiply

## Endpoint

- **Method:** `POST`
- **Path:** `/badges/`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Create Badge List](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Badge list label. |
| `list[]` | body | `array<object>` | yes | Badges to include in the badge list. |
