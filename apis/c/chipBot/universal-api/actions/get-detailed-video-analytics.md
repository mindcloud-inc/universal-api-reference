# ChipBot: Get Detailed Video Analytics



```
GET https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-detailed-video-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-detailed-video-analytics?connectionId=$CONNECTION_ID&endDate=string&startDate=string&tz=string&videoExpId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "startDate": "string",
  "tz": "string",
  "videoExpId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-detailed-video-analytics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | yes | The report end timestamp in ISO-8601 format. |
| `startDate` | string | yes | The report start timestamp in ISO-8601 format. |
| `tz` | string | yes | The timezone offset used by the report window, for example -06:00. |
| `videoExpId` | string | yes | The video experience identifier, for example videxp_xxx. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "countries": {
          "current": [
            {
              "count": 1,
              "country": "string"
            }
          ]
        },
        "videoExpAvgViewTime": {
          "current": [
            {
              "count": 1,
              "date": "2026-05-07T12:00:00.000Z"
            }
          ]
        },
        "videoExpDesktopViews": {
          "current": [
            {
              "count": 1,
              "date": "2026-05-07T12:00:00.000Z"
            }
          ]
        },
        "videoExpMobileViews": {
          "current": [
            {
              "count": 1,
              "date": "2026-05-07T12:00:00.000Z"
            }
          ]
        },
        "videoExpViews": {
          "current": [
            {
              "count": 1,
              "date": "2026-05-07T12:00:00.000Z"
            }
          ]
        }
      },
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Detailed analytics payload. |
| `data.countries.current` | array<object> | Country distribution. |
| `data.countries.current[].count` | number | Country count. |
| `data.countries.current[].country` | string | Country code. |
| `data.videoExpAvgViewTime.current` | array<object> | Current average-view-time series. |
| `data.videoExpAvgViewTime.current[].count` | number | Series count value. |
| `data.videoExpAvgViewTime.current[].date` | date | Series date. |
| `data.videoExpDesktopViews.current` | array<object> | Current desktop-view series. |
| `data.videoExpDesktopViews.current[].count` | number | Series count value. |
| `data.videoExpDesktopViews.current[].date` | date | Series date. |
| `data.videoExpMobileViews.current` | array<object> | Current mobile-view series. |
| `data.videoExpMobileViews.current[].count` | number | Series count value. |
| `data.videoExpMobileViews.current[].date` | date | Series date. |
| `data.videoExpViews.current` | array<object> | Current view series. |
| `data.videoExpViews.current[].count` | number | Series count value. |
| `data.videoExpViews.current[].date` | date | Series date. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId/reporting/detailed` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-detailed-video-analytics.md) for the provider-specific parameters and requirements.

