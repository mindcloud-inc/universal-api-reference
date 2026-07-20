# Permit.io: Get API Key Scope



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-api-key-scope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-api-key-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-api-key-scope?${params}`, {
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
      "environmentId": "string",
      "organizationId": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environmentId` | string | Environment ID for the current API key scope |
| `organizationId` | string | Organization ID for the current API key scope |
| `projectId` | string | Project ID for the current API key scope |

## Native endpoint

Through the native Permit.io API, this operation is `GET /v2/api-key/scope` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key-scope.md) for the provider-specific parameters and requirements.

