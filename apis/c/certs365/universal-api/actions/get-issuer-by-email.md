# Certs 365: Get Issuer By Email

Retrieves issuer details from Certs 365 by email.

```
GET https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-issuer-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-issuer-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-issuer-by-email?${params}`, {
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
| `email` | string | yes | Issuer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `POST /api/get-issuer-by-email` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issuer-by-email.md) for the provider-specific parameters and requirements.

