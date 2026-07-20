# List Opted-Out SMS Subscribers by Date with WaiverFile

Retrieves opted-out SMS subscribers from WaiverFile by opt-out date.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetOptedOutSubscribersByOptOutDate`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [List Opted-Out SMS Subscribers by Date](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDateUTC` | query | `date` | yes |
| `endDateUTC` | query | `date` | yes |
