# Pinata: Get Gateway Domain Availability

Retrieves gateway domain availability from Pinata.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-gateway-domain-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-gateway-domain-availability?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-gateway-domain-availability?${params}`, {
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
| `domain` | string | yes | Gateway subdomain to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean | Whether the requested gateway domain already exists. |

## Native endpoint

Through the native Pinata API, this operation is `GET /v3/gateways/exists/:domain` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gateway-domain-availability.md) for the provider-specific parameters and requirements.

