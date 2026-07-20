# Yutori: List Scouts

Retrieves scouting tasks for the current Yutori account.

```
GET https://connect.mindcloud.co/v1/universal/yutori/latest/actions/list-scouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/list-scouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yutori/latest/actions/list-scouts?${params}`, {
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
| `status` | string | no | Optional scout status filter. |
| `includeAllSources` | boolean | no | Whether to include all source types. |
| `pageSize` | number | no | Maximum number of scouts to return. |
| `cursor` | string | no | Cursor for the next page of scouts. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yutori API returns.

## Native endpoint

Through the native Yutori API, this operation is `GET /v1/scouting/tasks` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scouts.md) for the provider-specific parameters and requirements.

