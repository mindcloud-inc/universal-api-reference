# Vercel: Get Domain Config

Retrieves a domain configuration from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-domain-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-domain-config?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-domain-config?${params}`, {
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
| `domain` | string | yes | The domain name to inspect configuration for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuredBy": "string",
      "misconfigured": true,
      "nameservers": [
        "Ava Chen"
      ],
      "recommendedCNAME": [
        {}
      ],
      "recommendedIPv4": [
        {}
      ],
      "serviceType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuredBy` | string |  |
| `misconfigured` | boolean |  |
| `nameservers` | array<string> |  |
| `recommendedCNAME` | array<object> |  |
| `recommendedIPv4` | array<object> |  |
| `serviceType` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `GET /v6/domains/:domain/config` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-config.md) for the provider-specific parameters and requirements.

