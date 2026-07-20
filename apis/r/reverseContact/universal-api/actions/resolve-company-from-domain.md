# Reverse Contact: Resolve Company From Domain



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/resolve-company-from-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/resolve-company-from-domain?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/resolve-company-from-domain?${params}`, {
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
| `domain` | string | yes | Company domain to resolve. |
| `webhookUrl` | string | no | HTTPS callback URL for async results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `webhookId` | string |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/resolve/companies/live` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-company-from-domain.md) for the provider-specific parameters and requirements.

