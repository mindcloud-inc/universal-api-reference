# PocketSmith: Get Trend Analysis For User

Retrieves trend analysis for a PocketSmith user.

```
GET https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-trend-analysis-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PocketSmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-trend-analysis-for-user?connectionId=$CONNECTION_ID&categories=string&endDate=string&interval=1&period=string&scenarios=string&startDate=string&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categories": "string",
  "endDate": "string",
  "interval": "1",
  "period": "string",
  "scenarios": "string",
  "startDate": "string",
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-trend-analysis-for-user?${params}`, {
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
| `categories` | string | yes | A comma-separated list of category IDs to analyse. |
| `endDate` | string | yes | The date to stop analysing the trend at. |
| `interval` | number | yes | The period interval to analyse in. |
| `period` | string | yes | The period to analyse in. |
| `scenarios` | string | yes | A comma-separated list of scenario IDs to analyse. |
| `startDate` | string | yes | The date to start analysing the trend from. |
| `userId` | number | yes | The unique identifier of the PocketSmith user. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PocketSmith API returns.

## Native endpoint

Through the native PocketSmith API, this operation is `GET /users/:id/trend_analysis` (base URL `https://api.pocketsmith.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trend-analysis-for-user.md) for the provider-specific parameters and requirements.

