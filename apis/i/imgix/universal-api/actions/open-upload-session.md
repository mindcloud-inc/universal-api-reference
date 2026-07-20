# imgix: Open Upload Session

Opens an upload session in imgix.

```
POST https://connect.mindcloud.co/v1/universal/imgix/latest/actions/open-upload-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/open-upload-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "originPath": "string",
  "sourceId": "69de49d580720625c04f9162"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imgix/latest/actions/open-upload-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "originPath": "string",
    "sourceId": "69de49d580720625c04f9162"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `originPath` | string | yes | The destination origin path for the large upload session. |
| `sourceId` | string | yes | The imgix source_id. Default: `69de49d580720625c04f9162`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "dateCreated": 1,
          "dateExpires": 1,
          "dateModified": 1,
          "id": "string",
          "originPath": "string",
          "sourceId": "string",
          "status": "string",
          "url": "https://example.com"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.dateCreated` | number |  |
| `data.attributes.dateExpires` | number |  |
| `data.attributes.dateModified` | number |  |
| `data.attributes.id` | string |  |
| `data.attributes.originPath` | string |  |
| `data.attributes.sourceId` | string |  |
| `data.attributes.status` | string |  |
| `data.attributes.url` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `POST sources/:sourceId/upload-sessions/create/:originPath` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-upload-session.md) for the provider-specific parameters and requirements.

