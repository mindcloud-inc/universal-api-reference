# Orshot: Get All Studio Templates



```
GET https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-all-studio-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-all-studio-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-all-studio-templates?${params}`, {
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
| `embedId` | string | no | Embed instance ID for user-specific filtering. Must be used together with Embed User ID. |
| `embedUserId` | string | no | User ID for template filtering. Must be used together with Embed ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canvasHeight": 1,
      "canvasWidth": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "embedUserId": "string",
      "id": 1,
      "modifications": [
        {}
      ],
      "name": "Ava Chen",
      "pagesData": [
        {}
      ],
      "thumbnailUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `canvasHeight` | number |  |
| `canvasWidth` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `embedUserId` | string |  |
| `id` | number |  |
| `modifications` | array<object> |  |
| `name` | string |  |
| `pagesData` | array<object> |  |
| `thumbnailUrl` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Orshot API, this operation is `GET /studio/templates/all` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-studio-templates.md) for the provider-specific parameters and requirements.

