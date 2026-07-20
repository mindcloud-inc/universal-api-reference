# Geral: Get Domain

Retrieves a custom domain from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-domain?connectionId=$CONNECTION_ID&domainId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-domain?${params}`, {
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
| `domainId` | number | yes | The domain ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_index_url": "https://example.com",
      "datetime": "2026-05-07T12:00:00.000Z",
      "host": "string",
      "id": 1,
      "is_enabled": true,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "scheme": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_index_url` | string | Custom index URL. |
| `datetime` | date | Creation timestamp. |
| `host` | string | Domain host. |
| `id` | number | Domain ID. |
| `is_enabled` | boolean | Whether the domain is enabled. |
| `last_datetime` | date | Last update timestamp. |
| `scheme` | string | Domain URL scheme. |

## Native endpoint

Through the native Geral API, this operation is `GET /domains/:domain_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

