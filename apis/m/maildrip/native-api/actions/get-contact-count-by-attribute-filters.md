# Get contact count by attribute filters with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/contacts/count`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Get contact count by attribute filters](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributeFilters` | query | `string` | yes | JSON array of filter objects. Format: [{"key":"plan","operator":"equals","value":"pro"}] |
