# Placid: Create Template

Creates a new template in Placid.

```
POST https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title for the new template. |
| `fromTemplate` | string | no | Existing template UUID to clone from. |
| `width` | number | no | Template width in pixels when creating from scratch. |
| `height` | number | no | Template height in pixels when creating from scratch. |
| `tags[]` | array<string> | no | Tags to attach to the template. |
| `customData` | object | no | Custom data to store on the template. |
| `addToCollections[]` | array<string> | no | Collection UUIDs that should include the new template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collections": [
        "string"
      ],
      "customData": "string",
      "height": 1,
      "layers": [
        {}
      ],
      "tags": [
        "string"
      ],
      "thumbnail": "string",
      "title": "string",
      "uuid": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections` | array<string> |  |
| `customData` | string |  |
| `height` | number |  |
| `layers` | array<object> |  |
| `tags` | array<string> |  |
| `thumbnail` | string |  |
| `title` | string |  |
| `uuid` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Placid API, this operation is `POST /api/rest/templates` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

