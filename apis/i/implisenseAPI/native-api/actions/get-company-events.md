# Get Company Events with Implisense

Retrieves company events from Implisense API.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:id/events`
- **Base URL:** `https://german-company-data.p.rapidapi.com`
- **Official documentation:** [Get Company Events](https://docs.implisense.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Implisense company identifier, for example DEVFCLQFW054. |
| `type` | query | `string` | no | Optional event type, such as BLOG or NEWS. |
| `category` | query | `string` | no | Optional event category code, such as MANAGEMENT_AND_TEAM. |
| `since` | query | `string` | no | Optional lower timestamp boundary for returned events. |
| `size` | query | `number` | no | Maximum number of events to return. |
