# Evervault: Retrieve Relay Custom Domain

Retrieves a relay custom domain from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-relay-custom-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-relay-custom-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-relay-custom-domain?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "customDomain": "string",
      "id": "string",
      "relay": "string",
      "status": "string",
      "updatedAt": 1,
      "validationRecord": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `customDomain` | string |  |
| `id` | string |  |
| `relay` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |
| `validationRecord` | object |  |

## Native endpoint

Through the native Evervault API, this operation is `GET /relays/{relay_id}/custom-domains/{id}` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-relay-custom-domain.md) for the provider-specific parameters and requirements.

