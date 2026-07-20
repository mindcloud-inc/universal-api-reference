# List Available Time Slots with SavvyCal

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links/:link_id/slots`
- **Base URL:** `https://api.savvycal.com`
- **Official documentation:** [List Available Time Slots](https://developers.savvycal.com/api/get-link-slots)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_id` | path | `string` | yes |
| `from` | query | `date` | no |
| `until` | query | `date` | no |
