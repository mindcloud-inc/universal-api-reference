# Add Badges To Badge List with Ubiqod by Skiply

## Endpoint

- **Method:** `POST`
- **Path:** `/badges/:badgeListId/codes`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Add Badges To Badge List](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badgeListId` | path | `string` | yes | Badge list ID. |
| `list[]` | body | `array<object>` | yes | Badges to add to the badge list. |
