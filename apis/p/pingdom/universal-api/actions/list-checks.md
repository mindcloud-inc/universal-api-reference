# Pingdom: List Checks



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-checks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-checks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-checks?${params}`, {
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
| `showEncryption` | boolean | no | Include the encryption setting for each check. |
| `includeTags` | boolean | no | Include the tag list for each check. |
| `includeSeverity` | boolean | no | Include the severity level for each check. |
| `tags` | string | no | Comma-separated tag list used to filter returned checks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "hostname": "Ava Chen",
      "id": 1,
      "ipv6": true,
      "lastdownend": 1,
      "lastdownstart": 1,
      "lasterrortime": 1,
      "lastresponsetime": 1,
      "lasttesttime": 1,
      "name": "Ava Chen",
      "resolution": 1,
      "status": "string",
      "tags": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | UNIX time when the check was created. |
| `hostname` | string | Target hostname. |
| `id` | number | Check identifier. |
| `ipv6` | boolean | Whether the check uses IPv6. |
| `lastdownend` | number | UNIX time when the last downtime ended. |
| `lastdownstart` | number | UNIX time when the last downtime started. |
| `lasterrortime` | number | UNIX time of the last error, when present. |
| `lastresponsetime` | number | Response time of the last test in milliseconds. |
| `lasttesttime` | number | UNIX time of the last executed test. |
| `name` | string | Check name. |
| `resolution` | number | Check interval in minutes. |
| `status` | string | Current check status. |
| `tags` | array<object> | Tags assigned to the check. |
| `type` | string | Check type. |

## Native endpoint

Through the native Pingdom API, this operation is `GET /checks` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checks.md) for the provider-specific parameters and requirements.

