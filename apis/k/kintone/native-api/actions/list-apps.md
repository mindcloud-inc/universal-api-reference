# List Apps with Kintone

Retrieves apps from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [List Apps](https://kintone.dev/en/docs/kintone/rest-api/apps/get-apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `list<number>` | no | Filter by one or more Kintone app IDs. Send multiple values as a array. |
| `codes` | query | `list<string>` | no | Filter by one or more Kintone app codes. Send multiple values as a array. |
| `name` | query | `string` | no | Filter by app name prefix. |
| `spaceIds` | query | `list<number>` | no | Filter by one or more Kintone space IDs. Send multiple values as a array. |
| `limit` | query | `number` | no | Maximum number of apps to return. |
| `offset` | query | `number` | no | Number of apps to skip before returning results. |
