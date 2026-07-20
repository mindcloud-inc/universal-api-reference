# Get User Details with Countly

Retrieves all user details from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [Get User Details](https://api.count.ly/reference/omethoduser_detailsuid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID that contains the user. |
| `uid` | query | `string` | yes | Countly user ID to fetch details for. |
| `period` | query | `string` | no | Countly reporting period for user details. |
