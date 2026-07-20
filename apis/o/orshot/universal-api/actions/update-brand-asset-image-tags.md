# Orshot: Update Brand Asset Image Tags



```
PUT https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-asset-image-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-asset-image-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-asset-image-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The brand asset image ID. |
| `tags[]` | array<string> | yes | The tags to set on the asset, replacing existing tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "directUrl": "https://example.com",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "id": 1,
      "meta": {},
      "tags": [
        "string"
      ],
      "userId": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the image asset was created. |
| `directUrl` | string | Direct URL for the stored image asset. |
| `fileName` | string | Stored filename for the image asset. |
| `fileSize` | number | Image asset file size in bytes. |
| `id` | number | Brand image asset identifier. |
| `meta` | object | Provider metadata returned for the image asset. |
| `tags` | array<string> | Tags assigned to the image asset. |
| `userId` | string | User that created the image asset. |
| `workspaceId` | number | Workspace that owns the image asset. |

## Native endpoint

Through the native Orshot API, this operation is `PATCH /brand-assets/images/update/:id` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-brand-asset-image-tags.md) for the provider-specific parameters and requirements.

