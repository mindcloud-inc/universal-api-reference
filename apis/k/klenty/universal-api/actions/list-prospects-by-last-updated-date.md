# Klenty: List Prospects By Last Updated Date

Retrieves prospects from Klenty by last updated date.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-last-updated-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-last-updated-date?connectionId=$CONNECTION_ID&lastUpdatedDateStart=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lastUpdatedDateStart": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-prospects-by-last-updated-date?${params}`, {
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
| `lastUpdatedDateEnd` | string | no | End date for the prospect last-updated filter. Runtime expects yyyy/mm/dd for this endpoint when provided. |
| `lastUpdatedDateStart` | string | yes | Start date for the prospect last-updated filter. Runtime expects yyyy/mm/dd for this endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Klenty API returns.

## Native endpoint

Through the native Klenty API, this operation is `GET /prospects` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prospects-by-last-updated-date.md) for the provider-specific parameters and requirements.

