# Apideck: Get consumer

Retrieves a consumer from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersone?connectionId=$CONNECTION_ID&consumer_id=%7B%7Bcredentials.consumerId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "consumer_id": "{{credentials.consumerId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersone?${params}`, {
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
| `consumer_id` | string | yes | Default: `{{credentials.consumerId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregated_request_count": 1,
      "application_id": "string",
      "connections": [
        {}
      ],
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
| `connections` | array<object> |  |
| `consumer_id` | string |  |
| `created` | string |  |
| `metadata` | object |  |
| `modified` | string |  |
| `request_count_updated` | string |  |
| `request_counts` | object |  |
| `services` | array<string> |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/consumers/:consumer_id` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/consumersone.md) for the provider-specific parameters and requirements.

