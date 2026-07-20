# ClickHouse: List API Keys



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-api-keys?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/list-api-keys?${params}`, {
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
| `organizationId` | string | yes | ID of the requested organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedRoles": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expireAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "ipAccessList": [
        {}
      ],
      "keySuffix": "string",
      "name": "Ava Chen",
      "roles": [
        "string"
      ],
      "state": "string",
      "usedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedRoles` | array<object> | Custom and system roles assigned to the API key. |
| `createdAt` | date | Timestamp the key was created. |
| `expireAt` | date | Timestamp the key expires, when present. |
| `id` | string | Unique API key ID. |
| `ipAccessList` | array<object> | IP addresses allowed to access the API using this key. |
| `keySuffix` | string | Last four characters of the key. |
| `name` | string | API key name. |
| `roles` | array<string> | Deprecated roles assigned to the key. |
| `state` | string | API key state. |
| `usedAt` | date | Timestamp the key was last used, when present. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/keys` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-keys.md) for the provider-specific parameters and requirements.

