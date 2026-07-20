# Mode: List Data Sources

List data sources connected to a Mode workspace.

```
GET https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-data-sources?${params}`, {
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
      "accountId": 1,
      "accountUsername": "Ava Chen",
      "adapter": "string",
      "asleep": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "database": "string",
      "description": "string",
      "displayName": "Ava Chen",
      "hasExpensiveSchemaUpdates": true,
      "host": "string",
      "id": 1,
      "Links": {},
      "name": "Ava Chen",
      "port": "string",
      "provider": "string",
      "public": true,
      "queryable": true,
      "softDeleted": true,
      "ssl": true,
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Mode account ID. |
| `accountUsername` | string | Mode account username. |
| `adapter` | string | Mode database adapter identifier. |
| `asleep` | boolean | Whether the data source is asleep. |
| `createdAt` | date | Creation timestamp. |
| `database` | string | Database name. |
| `description` | string | Data source description. |
| `displayName` | string | Display name for the data source. |
| `hasExpensiveSchemaUpdates` | boolean | Whether schema updates are expensive for this data source. |
| `host` | string | Database host. |
| `id` | number | Mode data source ID. |
| `Links` | object | Mode HAL links. |
| `name` | string | Data source name. |
| `port` | string | Database port. |
| `provider` | string | Provider name. |
| `public` | boolean | Whether the data source is public. |
| `queryable` | boolean | Whether the data source can be queried. |
| `softDeleted` | boolean | Whether the data source is soft deleted. |
| `ssl` | boolean | Whether SSL is enabled. |
| `token` | string | Mode data source token. |
| `updatedAt` | date | Last update timestamp. |
| `vendor` | string | Vendor name. |

## Native endpoint

Through the native Mode API, this operation is `GET /data_sources` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-sources.md) for the provider-specific parameters and requirements.

