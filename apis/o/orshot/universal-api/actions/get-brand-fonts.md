# Orshot: Get Brand Fonts



```
GET https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-brand-fonts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-brand-fonts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-brand-fonts?${params}`, {
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
| `tag` | string | no | Filter fonts by tag. |

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
| `createdAt` | date | Timestamp when the font asset was created. |
| `directUrl` | string | Direct URL for the stored custom font file. |
| `fileName` | string | Stored filename for the custom font asset. |
| `fileSize` | number | Font asset file size in bytes. |
| `id` | number | Custom font asset identifier. |
| `tags` | array<string> | Tags assigned to the font asset. |
| `userId` | string | User that created the font asset. |
| `workspaceId` | number | Workspace that owns the font asset. |

## Native endpoint

Through the native Orshot API, this operation is `GET /brand-assets/fonts/get` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brand-fonts.md) for the provider-specific parameters and requirements.

