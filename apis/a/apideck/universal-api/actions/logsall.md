# Apideck: Get all consumer request logs

Retrieves consumer request logs from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/logsall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/logsall?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/logsall?${params}`, {
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
| `cursor` | string | no |  |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_style": "string",
      "base_url": "https://example.com",
      "child_request": true,
      "consumer_id": "string",
      "duration": 1,
      "error_message": "string",
      "execution": 1,
      "has_children": true,
      "http_method": "string",
      "id": "string",
      "latency": 1,
      "operation": {},
      "parent_id": "string",
      "path": "string",
      "sandbox": true,
      "service": {},
      "source_ip": "string",
      "status_code": 1,
      "success": true,
      "timestamp": "string",
      "unified_api": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_style` | string |  |
| `base_url` | string |  |
| `child_request` | boolean |  |
| `consumer_id` | string |  |
| `duration` | number |  |
| `error_message` | string |  |
| `execution` | number |  |
| `has_children` | boolean |  |
| `http_method` | string |  |
| `id` | string |  |
| `latency` | number |  |
| `operation` | object |  |
| `parent_id` | string |  |
| `path` | string |  |
| `sandbox` | boolean |  |
| `service` | object |  |
| `source_ip` | string |  |
| `status_code` | number |  |
| `success` | boolean |  |
| `timestamp` | string |  |
| `unified_api` | string |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/logs` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/logsall.md) for the provider-specific parameters and requirements.

