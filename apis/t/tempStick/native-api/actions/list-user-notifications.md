# List User Notifications with Temp Stick

Retrieves the last seven days of Temp Stick user notifications.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/notifications`
- **Base URL:** `https://tempstickapi.com/api/v1`
- **Official documentation:** [List User Notifications](https://tempstickapi.com/docs/#api-Alerts-Get_User_Notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items_per_page` | query | `number` | yes | Maximum 100 items per page |
| `page` | query | `number` | yes | Page number |
