# CleverReach: List Report Receivers by State

Retrieves report receivers from CleverReach by delivery state.

```
GET https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-report-receivers-by-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CleverReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-report-receivers-by-state?connectionId=$CONNECTION_ID&id=string&state=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "state": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-report-receivers-by-state?${params}`, {
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
| `id` | string | yes | Report ID/Mailing ID. |
| `state` | string | yes | State to get. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `linkid` | string | no | ID of link that was clicked on. |
| `from` | number | no | Timestamp of earliest event of state. |
| `to` | number | no | Timestamp of latest event of state. |
| `detail` | number | no | Detail depth (bitwise combinable) (0: none, 1: events, 2: orders, 4: tags). Default: `0`. |
| `pagesize` | number | no | Max items. Default: `50`. |
| `page` | number | no | Page. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CleverReach API returns.

## Native endpoint

Through the native CleverReach API, this operation is `GET /v3/reports.json/:id/receivers/:state` (base URL `https://rest.cleverreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-report-receivers-by-state.md) for the provider-specific parameters and requirements.

