# Vortex: Configure Autojoin Domains



```
POST https://connect.mindcloud.co/v1/universal/vortex/latest/actions/configure-autojoin-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vortex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/configure-autojoin-domains" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vortex/latest/actions/configure-autojoin-domains', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "autojoinDomains": [
        {
          "domain": "string",
          "id": "string"
        }
      ],
      "invitation": {
        "id": "string",
        "scope": "string",
        "scopeType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autojoinDomains[].domain` | string |  |
| `autojoinDomains[].id` | string |  |
| `invitation.id` | string |  |
| `invitation.scope` | string |  |
| `invitation.scopeType` | string |  |

## Native endpoint

Through the native Vortex API, this operation is `POST /api/v1/invitations/autojoin` (base URL `https://api.vortexsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/configure-autojoin-domains.md) for the provider-specific parameters and requirements.

