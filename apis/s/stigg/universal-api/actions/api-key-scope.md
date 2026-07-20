# Stigg: API Key Scope



```
GET https://connect.mindcloud.co/v1/universal/stigg/latest/actions/api-key-scope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stigg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stigg/latest/actions/api-key-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stigg/latest/actions/api-key-scope?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "name": "Ava Chen",
      "refId": "string",
      "status": "string",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `displayName` | string | Human-readable display name. |
| `id` | string | Stigg object ID or result identifier. |
| `items` | array<object> | Returned objects for list responses. |
| `message` | string | Provider message or operation detail. |
| `name` | string | Result name. |
| `refId` | string | Stigg reference ID when present. |
| `status` | string | Result status. |
| `success` | boolean | Whether the operation completed successfully. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Stigg API, this operation is `POST /graphql` (base URL `https://api.stigg.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/api-key-scope.md) for the provider-specific parameters and requirements.

