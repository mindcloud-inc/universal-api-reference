# Miro: Get Access Token Context

Retrieves access token context from Miro.

```
GET https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-access-token-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Miro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-access-token-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-access-token-context?${params}`, {
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
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "organization": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "scopes": [
        "string"
      ],
      "team": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "type": "string",
      "user": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organization.type` | string |  |
| `scopes` | array<string> |  |
| `team.id` | string |  |
| `team.name` | string |  |
| `team.type` | string |  |
| `type` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.type` | string |  |

## Native endpoint

Through the native Miro API, this operation is `GET https://api.miro.com/v1/oauth-token` (base URL `https://api.miro.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-token-context.md) for the provider-specific parameters and requirements.

