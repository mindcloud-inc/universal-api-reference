# List Prospects By Last Updated Date with Klenty

Retrieves prospects from Klenty by last updated date.

## Endpoint

- **Method:** `GET`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [List Prospects By Last Updated Date](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_b8930ef4b8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastUpdatedDateEnd` | query | `string` | no | End date for the prospect last-updated filter. Runtime expects yyyy/mm/dd for this endpoint when provided. |
| `lastUpdatedDateStart` | query | `string` | yes | Start date for the prospect last-updated filter. Runtime expects yyyy/mm/dd for this endpoint. |
