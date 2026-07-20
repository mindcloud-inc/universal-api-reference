# Get Forms with TalentLyft

Retrieves all forms from TalentLyft.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/forms`
- **Base URL:** `https://api.talentlyft.com`
- **Official documentation:** [Get Forms](https://developers.talentlyft.com/customer-api-reference/forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to return. |
| `perPage` | query | `number` | no | Number of results to return per page. |
| `contains` | query | `string` | no | Filter forms whose name contains this value. |
