# Orshot: Get Studio Template



```
GET https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-studio-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-studio-template?connectionId=$CONNECTION_ID&templateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-studio-template?${params}`, {
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
| `templateId` | number | yes | The unique ID of the template to fetch. |

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
      "modificationsJson": {},
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
| `modificationsJson` | object |  |
| `name` | string |  |
| `pagesData` | array<object> |  |
| `thumbnailUrl` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Orshot API, this operation is `GET /studio/templates/:templateId` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-studio-template.md) for the provider-specific parameters and requirements.

