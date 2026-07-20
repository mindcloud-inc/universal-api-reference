# Placid: Update Template

Updates an existing template in Placid.

```
PUT https://connect.mindcloud.co/v1/universal/placid/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/placid/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placid/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateUuid` | string | yes | UUID of the template to update. |
| `title` | string | no | Updated title for the template. |
| `tags[]` | array<string> | no | Updated tags for the template. |
| `customData` | object | no | Updated custom data for the template. |

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

Through the native Placid API, this operation is `PATCH /api/rest/templates/:templateUuid` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

