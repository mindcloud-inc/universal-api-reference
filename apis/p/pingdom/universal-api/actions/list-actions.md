# Pingdom: List Actions



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-actions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-actions?${params}`, {
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
| `from` | number | no | Only include actions generated later than this UNIX timestamp. |
| `to` | number | no | Only include actions generated earlier than this UNIX timestamp. |
| `checkIds` | string | no | Comma-separated list of check identifiers to filter actions. |
| `userIds` | string | no | Comma-separated list of user identifiers to filter actions. |
| `status` | string | no | Comma-separated list of action statuses to include. |
| `via` | string | no | Comma-separated list of delivery mediums to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charged": "string",
      "checkid": "string",
      "messagefull": "string",
      "messageshort": "string",
      "sentto": "string",
      "status": "string",
      "time": "string",
      "userid": "string",
      "username": "Ava Chen",
      "via": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charged` | string | Whether the account was charged for the alert message. |
| `checkid` | string | Identifier of the related check. |
| `messagefull` | string | Full alert message body. |
| `messageshort` | string | Short message summary. |
| `sentto` | string | Target address or phone number. |
| `status` | string | Alert delivery status. |
| `time` | string | UNIX time when the alert action was generated. |
| `userid` | string | Identifier of alerted user. |
| `username` | string | Name of alerted user. |
| `via` | string | Alert delivery medium. |

## Native endpoint

Through the native Pingdom API, this operation is `GET /actions` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-actions.md) for the provider-specific parameters and requirements.

