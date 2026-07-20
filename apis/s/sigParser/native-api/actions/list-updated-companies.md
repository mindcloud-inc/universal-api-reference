# List Updated Companies with SigParser

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Companies`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [List Updated Companies](https://ipaas.sigparser.com/v1#get-api-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastmodified_after` | query | `number` | yes | Only return companies changed since this lastmodified value. |
| `details_lastmodified_after` | query | `number` | no | Only return companies whose detail fields changed since this lastmodified value. |
| `take` | query | `number` | no | How many company records to return. Minimum 25, maximum 250. |
