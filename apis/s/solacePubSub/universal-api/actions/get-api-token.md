# Solace PubSub+: Get API Token

Retrieves an API token from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-api-token?connectionId=$CONNECTION_ID&tokenId=vrov6hux820" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tokenId": "vrov6hux820"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-api-token?${params}`, {
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
| `tokenId` | string | yes | Unique Solace Cloud API token identifier. Default: `vrov6hux820`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "permissions": [
        "string"
      ],
      "resourceAssignments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique API token identifier. |
| `name` | string | API token name. |
| `organizationId` | string | Solace Cloud organization identifier. |
| `permissions` | array<string> | Permission identifiers assigned to the token. |
| `resourceAssignments` | array<object> | Resource assignments attached to the token. |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/platform/apiTokens/{tokenId}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-token.md) for the provider-specific parameters and requirements.

