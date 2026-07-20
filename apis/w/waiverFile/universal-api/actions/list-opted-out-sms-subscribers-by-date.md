# WaiverFile: List Opted-Out SMS Subscribers by Date

Retrieves opted-out SMS subscribers from WaiverFile by opt-out date.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-opted-out-sms-subscribers-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-opted-out-sms-subscribers-by-date?connectionId=$CONNECTION_ID&startDateUTC=2026-05-07T12%3A00%3A00.000Z&endDateUTC=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateUTC": "2026-05-07T12:00:00.000Z",
  "endDateUTC": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-opted-out-sms-subscribers-by-date?${params}`, {
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
| `startDateUTC` | date | yes |  |
| `endDateUTC` | date | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaiverFile API returns.

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetOptedOutSubscribersByOptOutDate` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opted-out-sms-subscribers-by-date.md) for the provider-specific parameters and requirements.

