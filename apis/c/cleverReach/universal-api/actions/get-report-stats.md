# CleverReach: Get Report Stats

Retrieves report statistics from CleverReach by reporting mode.

```
GET https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-report-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CleverReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-report-stats?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-report-stats?${params}`, {
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
| `id` | string | yes | ID of Report/Mailing. |
| `mode` | string | no | Mode of statistics. One of: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Default: `full`. |
| `start` | string | no | Startdate unixtimestamp (only for mode daily). Default: `0`. |
| `end` | string | no | Enddate unixtimestamp (only for mode daily). Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CleverReach API returns.

## Native endpoint

Through the native CleverReach API, this operation is `GET /v3/reports.json/:id/stats/:mode` (base URL `https://rest.cleverreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-stats.md) for the provider-specific parameters and requirements.

