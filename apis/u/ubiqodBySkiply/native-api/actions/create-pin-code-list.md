# Create PIN Code List with Ubiqod by Skiply

## Endpoint

- **Method:** `POST`
- **Path:** `/pincodes/`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Create PIN Code List](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | PIN code list label. |
| `list[]` | body | `array<object>` | yes | PIN codes to include in the list. |
