# Count Links with Rebrandly

Retrieves the number of links in Rebrandly.

## Endpoint

- **Method:** `GET`
- **Path:** `/links/count`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Count Links](https://developers.rebrandly.com/docs/counting-your-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `favourite` | query | `boolean` | no | Filter links by favourite status. |
| `domain.id` | query | `string` | no | Filter links by branded domain ID. |
