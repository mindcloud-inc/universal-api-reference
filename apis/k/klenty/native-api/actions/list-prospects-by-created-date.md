# List Prospects By Created Date with Klenty

Retrieves prospects from Klenty by created date.

## Endpoint

- **Method:** `GET`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [List Prospects By Created Date](https://support.klenty.com/en/articles/8193357-klenty-s-get-api-s#h_e9d493f674)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | Start date in YYYY/MM/DD format. |
| `endDate` | query | `string` | no | End date in YYYY/MM/DD format. |
