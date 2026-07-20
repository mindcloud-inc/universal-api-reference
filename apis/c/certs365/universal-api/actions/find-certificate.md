# Certs 365: Find Certificate

Finds a certificate in Certs 365 by ID or name.

```
GET https://connect.mindcloud.co/v1/universal/certs365/latest/actions/find-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/find-certificate?connectionId=$CONNECTION_ID&email=ava%40example.com&input=string&type=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "input": "string",
  "type": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/find-certificate?${params}`, {
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
| `input` | string | yes | Certificate ID or name to search for. |
| `type` | number | yes | Search type: 1 for renew, 2 for reactivate, 3 for revoke. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `data` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `POST /api/get-issue` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-certificate.md) for the provider-specific parameters and requirements.

