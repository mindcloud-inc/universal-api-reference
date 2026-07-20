# List SMS Subscribers by Date with WaiverFile

Retrieves SMS subscribers from WaiverFile by opt-in date.

## Endpoint

- **Method:** `GET`
- **Path:** `/GetSubscribersByDate`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [List SMS Subscribers by Date](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startDateUTC` | query | `date` | yes |
| `endDateUTC` | query | `date` | yes |
