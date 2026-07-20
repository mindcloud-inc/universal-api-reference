# Certifier: List Attributes

Retrieves all available attributes from Certifier.

```
GET https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-attributes?${params}`, {
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
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen",
      "parent": "string",
      "tag": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `parent` | string |  |
| `tag` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Certifier API, this operation is `GET /attributes` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attributes.md) for the provider-specific parameters and requirements.

