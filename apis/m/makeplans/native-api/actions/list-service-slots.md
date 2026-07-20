# List Service Slots with Makeplans

Retrieves available service slots from Makeplans.

## Endpoint

- **Method:** `GET`
- **Path:** `/services/:serviceId/slots`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [List Service Slots](https://developer.makeplans.com/endpoints/slots/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceId` | path | `number` | yes | The Makeplans service ID. |
| `from` | query | `date` | no | Start date for slot lookup. Defaults to today. |
| `to` | query | `date` | no | End date for slot lookup. Defaults to today. |
