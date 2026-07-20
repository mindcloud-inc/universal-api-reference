# Rye: Get Brand By Domain

Finds a brand in Rye by domain.

```
GET https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-brand-by-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-brand-by-domain?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-brand-by-domain?${params}`, {
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
| `domain` | string | yes | Domain name to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "marketplace": "string",
      "supported": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `marketplace` | string |  |
| `supported` | boolean |  |

## Native endpoint

Through the native Rye API, this operation is `GET /api/v1/brands/domain/{domain}` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brand-by-domain.md) for the provider-specific parameters and requirements.

