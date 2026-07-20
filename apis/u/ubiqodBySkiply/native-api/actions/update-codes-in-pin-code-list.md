# Update Codes In PIN Code List with Ubiqod by Skiply

## Endpoint

- **Method:** `PATCH`
- **Path:** `/pincodes/:pinCodeListId/codes`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Update Codes In PIN Code List](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pinCodeListId` | path | `string` | yes | PIN code list ID. |
| `list[]` | body | `array<object>` | yes | PIN codes to replace in the list. |
