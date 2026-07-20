# Delete Codes From PIN Code List with Ubiqod by Skiply

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pincodes/:pinCodeListId/codes`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Delete Codes From PIN Code List](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pinCodeListId` | path | `string` | yes | PIN code list ID. |
| `codes[]` | body | `array<string>` | yes | PIN codes to delete from the list. |
