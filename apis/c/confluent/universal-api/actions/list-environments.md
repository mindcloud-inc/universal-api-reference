# Confluent: List Environments

Retrieves environments from your Confluent Cloud organization.

```
GET https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluent/latest/actions/list-environments?${params}`, {
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
      "apiVersion": "string",
      "data": [
        {
          "displayName": "Ava Chen",
          "id": "string",
          "streamGovernanceConfig": {}
        }
      ],
      "kind": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `data` | array<object> |  |
| `data[].displayName` | string |  |
| `data[].id` | string |  |
| `data[].streamGovernanceConfig` | object |  |
| `kind` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Confluent API, this operation is `GET /org/v2/environments` (base URL `https://api.confluent.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

