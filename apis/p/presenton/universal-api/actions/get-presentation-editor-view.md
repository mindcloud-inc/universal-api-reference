# Presenton: Get Presentation Editor View



```
GET https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-presentation-editor-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-presentation-editor-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-presentation-editor-view?${params}`, {
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
| `id` | string | yes | The presentation ID to retrieve in editor view. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "language": "string",
      "nSlides": 1,
      "slides": [
        [
          {}
        ]
      ],
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `language` | string |  |
| `nSlides` | number |  |
| `slides[]` | array<object> |  |
| `slides[].id` | string |  |
| `slides[].index` | number |  |
| `slides[].layout` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Presenton API, this operation is `GET /api/v1/ppt/presentation/:id/ui` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-presentation-editor-view.md) for the provider-specific parameters and requirements.

