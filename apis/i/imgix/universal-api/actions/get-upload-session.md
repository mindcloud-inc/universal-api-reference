# imgix: Get Upload Session

Retrieves an upload session from imgix.

```
GET https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-upload-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-upload-session?connectionId=$CONNECTION_ID&sessionId=string&sourceId=69de49d580720625c04f9162" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "sourceId": "69de49d580720625c04f9162"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-upload-session?${params}`, {
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
| `sessionId` | string | yes | The upload session id. |
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
          "status": "string"
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
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `GET sources/:sourceId/upload-sessions/status/:sessionId` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-session.md) for the provider-specific parameters and requirements.

