# LaunchDarkly: List Audit Log

Retrieves audit log entries from LaunchDarkly.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-audit-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-audit-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-audit-log?${params}`, {
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
      "accesses": [
        {}
      ],
      "accountId": "string",
      "date": 1,
      "description": "string",
      "id": "string",
      "kind": "string",
      "links": {},
      "member": {},
      "name": "Ava Chen",
      "shortDescription": "string",
      "target": {},
      "title": "string",
      "token": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accesses` | array<object> |  |
| `accountId` | string |  |
| `date` | number |  |
| `description` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `links` | object |  |
| `member` | object |  |
| `name` | string |  |
| `shortDescription` | string |  |
| `target` | object |  |
| `title` | string |  |
| `token` | object |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /auditlog` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audit-log.md) for the provider-specific parameters and requirements.

