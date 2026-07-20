# Edusign: List Document Templates

Retrieves document templates from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-document-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-document-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-document-templates?${params}`, {
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
      "result": {
        "templates": [
          {
            "attachedDocuments": [
              "string"
            ],
            "dateCreated": "string",
            "dateUpdated": "string",
            "id": "string",
            "imageUrl": "https://example.com",
            "inputs": [
              {
                "category": "string",
                "id": 1,
                "index": 1,
                "label": "string",
                "page": "string",
                "position": {
                  "height": 1,
                  "width": 1,
                  "x": 1,
                  "y": 1
                },
                "required": true,
                "type": "string"
              }
            ],
            "name": "Ava Chen",
            "schoolId": "string",
            "template": "string",
            "thumbnailUrl": "https://example.com",
            "type": 1
          }
        ],
        "total": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.templates` | array<object> |  |
| `result.templates[].attachedDocuments` | array<string> |  |
| `result.templates[].dateCreated` | string |  |
| `result.templates[].dateUpdated` | string |  |
| `result.templates[].id` | string |  |
| `result.templates[].imageUrl` | string |  |
| `result.templates[].inputs` | array<object> |  |
| `result.templates[].inputs[].category` | string |  |
| `result.templates[].inputs[].id` | number |  |
| `result.templates[].inputs[].index` | number |  |
| `result.templates[].inputs[].label` | string |  |
| `result.templates[].inputs[].page` | string |  |
| `result.templates[].inputs[].position` | object |  |
| `result.templates[].inputs[].position.height` | number |  |
| `result.templates[].inputs[].position.width` | number |  |
| `result.templates[].inputs[].position.x` | number |  |
| `result.templates[].inputs[].position.y` | number |  |
| `result.templates[].inputs[].required` | boolean |  |
| `result.templates[].inputs[].type` | string |  |
| `result.templates[].name` | string |  |
| `result.templates[].schoolId` | string |  |
| `result.templates[].template` | string |  |
| `result.templates[].thumbnailUrl` | string |  |
| `result.templates[].type` | number |  |
| `result.total` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v2/documents/templates` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-templates.md) for the provider-specific parameters and requirements.

