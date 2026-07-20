# Update Badge List with Ubiqod by Skiply

## Endpoint

- **Method:** `PATCH`
- **Path:** `/badges/:badgeListId`
- **Base URL:** `https://api.ubiqod.com`
- **Official documentation:** [Update Badge List](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badgeListId` | path | `string` | yes | Badge list ID. |
| `label` | body | `string` | yes | Updated badge list label. |
