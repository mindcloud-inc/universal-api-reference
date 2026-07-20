# Kommo: List Notes For Entity



```
GET https://connect.mindcloud.co/v1/universal/kommo/latest/actions/list-notes-for-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kommo/latest/actions/list-notes-for-entity?connectionId=$CONNECTION_ID&entityType=leads&entityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "leads",
  "entityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kommo/latest/actions/list-notes-for-entity?${params}`, {
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
| `entity_id` | string | no | Required path parameter for List Notes For Entity. |
| `entity_type` | string | no | Required path parameter for List Notes For Entity. |
| `entityType` | string | yes | The entity type segment used in the path. Example: `leads`. |
| `entityId` | number | yes | The parent entity identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "name": "Ava Chen",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp when returned by Kommo. |
| `id` | string | Unique identifier returned by Kommo. |
| `links.self.href` | string | Kommo API resource URL when returned in links. |
| `name` | string | Display name or title when returned by Kommo. |
| `updatedAt` | number | Last update timestamp when returned by Kommo. |

## Native endpoint

Through the native Kommo API, this operation is `GET /:entity_type/:entity_id/notes` (base URL `https://{{credentials.authorizeRequest.referer}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes-for-entity.md) for the provider-specific parameters and requirements.

