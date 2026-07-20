# Vortex: Get Autojoin Domains By Scope



```
GET https://connect.mindcloud.co/v1/universal/vortex/latest/actions/get-autojoin-domains-by-scope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vortex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/get-autojoin-domains-by-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vortex/latest/actions/get-autojoin-domains-by-scope?${params}`, {
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

Through the native Vortex API, this operation is `GET /api/v1/invitations/by-scope/{scopeType}/{scope}/autojoin` (base URL `https://api.vortexsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-autojoin-domains-by-scope.md) for the provider-specific parameters and requirements.

