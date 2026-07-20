# Clockify: List Updated Entities (Experimental)

Lists experimentally tracked updated entities in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-updated-entities-experimental
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-updated-entities-experimental?connectionId=$CONNECTION_ID&workspaceId=string&type%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "type[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-updated-entities-experimental?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `type[]` | array<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end` | string | no | Example: `2026-01-01`. |
| `start` | string | no | Example: `2026-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/entities/updated` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-updated-entities-experimental.md) for the provider-specific parameters and requirements.

