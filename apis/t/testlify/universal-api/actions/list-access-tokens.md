# Testlify: List Access Tokens

Retrieves Testlify access tokens with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-access-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-access-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-access-tokens?${params}`, {
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
| `q` | string | no | Search text for access tokens. |
| `createdBy` | string | no | Filter by creator. |
| `status` | string | no | Filter by token status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "createdBy": "string",
      "expiration": "string",
      "id": "string",
      "lastUsed": "string",
      "modified": "string",
      "note": "string",
      "orgId": "string",
      "status": "string",
      "workspaceUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `createdBy` | string |  |
| `expiration` | string |  |
| `id` | string |  |
| `lastUsed` | string |  |
| `modified` | string |  |
| `note` | string |  |
| `orgId` | string |  |
| `status` | string |  |
| `workspaceUrl` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/workspace/accesstokens` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-access-tokens.md) for the provider-specific parameters and requirements.

