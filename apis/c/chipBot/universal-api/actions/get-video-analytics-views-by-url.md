# ChipBot: Get Video Analytics Views by URL



```
GET https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-video-analytics-views-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-video-analytics-views-by-url?connectionId=$CONNECTION_ID&endDate=string&startDate=string&tz=string&videoExpId=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-video-analytics-views-by-url?${params}`, {
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
        "viewsByUrl": {
          "current": [
            {
              "count": 1,
              "url": "https://example.com"
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
| `data` | object | Views-by-URL payload. |
| `data.viewsByUrl.current` | array<object> | Current URL view rows. |
| `data.viewsByUrl.current[].count` | number | View count. |
| `data.viewsByUrl.current[].url` | string | Reported page URL. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId/reporting/views-by-url` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-analytics-views-by-url.md) for the provider-specific parameters and requirements.

