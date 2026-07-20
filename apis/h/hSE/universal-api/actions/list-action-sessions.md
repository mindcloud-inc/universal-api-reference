# 4HSE: List Action Sessions

Retrieves action sessions from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-sessions?${params}`, {
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
      "actionId": "string",
      "actionName": "Ava Chen",
      "actionSessionId": "string",
      "actionType": "string",
      "dateBegin": "2026-05-07T12:00:00.000Z",
      "dateExpire": "2026-05-07T12:00:00.000Z",
      "officeName": "Ava Chen",
      "permission": "string",
      "subtenantId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | string | Action identifier |
| `actionName` | string | Action name |
| `actionSessionId` | string | Action session identifier |
| `actionType` | string | Action type |
| `dateBegin` | date | Session start date |
| `dateExpire` | date | Session end date |
| `officeName` | string | Office name |
| `permission` | string | Permission level |
| `subtenantId` | string | Office identifier |
| `tenantId` | string | Project identifier |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/action-session/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-action-sessions.md) for the provider-specific parameters and requirements.

