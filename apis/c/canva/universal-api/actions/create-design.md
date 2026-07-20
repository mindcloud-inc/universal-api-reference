# Canva: Create Design

Creates a new design in Canva.

```
POST https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designType.type": "custom"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designType.type": "custom"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designType` | object | no | The design type to create. |
| `designType.type` | list | yes | Choose whether the new design uses a preset type or custom dimensions. One of: `custom`, `preset`. |
| `designType.name` | list | no | Preset Canva design type name. One of: `doc`, `presentation`, `whiteboard`. |
| `designType.width` | number | no | Width in pixels for a custom design type. |
| `designType.height` | number | no | Height in pixels for a custom design type. |
| `assetId` | string | no | Optional asset ID to insert into the created design. |
| `title` | string | no | Optional title for the new design. |

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

Through the native Canva API, this operation is `POST /v1/designs` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-design.md) for the provider-specific parameters and requirements.

