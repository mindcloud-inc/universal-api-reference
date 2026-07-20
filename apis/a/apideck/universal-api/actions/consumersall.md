# Apideck: Get all consumers

Retrieves all consumers from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersall?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersall?${params}`, {
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
| `filter` | object | no |  |
| `cursor` | string | no | Cursor to start from for the next page. |
| `limit` | number | no | Number of results to return. Minimum 1, maximum 200. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregated_request_count": 1,
      "application_id": "string",
      "consumer_id": "string",
      "created": "string",
      "metadata": {},
      "modified": "string",
      "request_count_updated": "string",
      "request_counts": {},
      "services": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregated_request_count` | number |  |
| `application_id` | string |  |
| `consumer_id` | string |  |
| `created` | string |  |
| `metadata` | object |  |
| `modified` | string |  |
| `request_count_updated` | string |  |
| `request_counts` | object |  |
| `services` | array<string> |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/consumers` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/consumersall.md) for the provider-specific parameters and requirements.

