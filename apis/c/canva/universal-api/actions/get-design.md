# Canva: Get Design

Retrieves details for a Canva design.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design?connectionId=$CONNECTION_ID&designId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design?${params}`, {
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
| `designId` | string | yes | The Canva design ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "design": {
        "createdAt": 1,
        "id": "string",
        "owner": {
          "teamId": "string",
          "userId": "string"
        },
        "pageCount": 1,
        "title": "string",
        "updatedAt": 1,
        "urls": {
          "editUrl": "https://example.com",
          "viewUrl": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `design` | object |  |
| `design.createdAt` | number |  |
| `design.id` | string |  |
| `design.owner` | object |  |
| `design.owner.teamId` | string |  |
| `design.owner.userId` | string |  |
| `design.pageCount` | number |  |
| `design.title` | string |  |
| `design.updatedAt` | number |  |
| `design.urls` | object |  |
| `design.urls.editUrl` | string |  |
| `design.urls.viewUrl` | string |  |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/designs/:designId` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-design.md) for the provider-specific parameters and requirements.

