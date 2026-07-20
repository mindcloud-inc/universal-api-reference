# Vortex: Delete Invitations By Scope



```
DELETE https://connect.mindcloud.co/v1/universal/vortex/latest/actions/delete-invitations-by-scope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vortex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/delete-invitations-by-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vortex/latest/actions/delete-invitations-by-scope?${params}`, {
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
      "scope": "string",
      "scopeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scope` | string |  |
| `scopeType` | string |  |

## Native endpoint

Through the native Vortex API, this operation is `DELETE /api/v1/invitations/by-scope/{scopeType}/{scope}` (base URL `https://api.vortexsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invitations-by-scope.md) for the provider-specific parameters and requirements.

