# Documently: List Webhook Logs

Retrieves webhook logs from Documently.

```
GET https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-webhook-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-webhook-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/list-webhook-logs?${params}`, {
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
| `project` | string | no | Project ID filter required by Documently. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "hydra:member": [
        {}
      ],
      "hydra:search": {},
      "hydra:totalItems": 1,
      "hydra:view": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `hydra:member` | array<object> |  |
| `hydra:search` | object |  |
| `hydra:totalItems` | number |  |
| `hydra:view` | object |  |

## Native endpoint

Through the native Documently API, this operation is `GET /webhook-logs` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-logs.md) for the provider-specific parameters and requirements.

