# Walmart: Get Account Settings

https://developer.walmart.com/us-marketplace/reference/getaccountlevelsettings

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-account-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-account-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-account-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarDayConfiguration": {
        "additionalDaysOff": [
          "string"
        ],
        "carrierWeekendCalendar": {
          "saturday": {
            "workingDay": true
          },
          "sunday": {
            "workingDay": true
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarDayConfiguration.additionalDaysOff[]` | string |  |
| `calendarDayConfiguration.carrierWeekendCalendar.saturday.workingDay` | boolean |  |
| `calendarDayConfiguration.carrierWeekendCalendar.sunday.workingDay` | boolean |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/account` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-settings.md) for the provider-specific parameters and requirements.

