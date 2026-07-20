# xMatters: Upload an EPIC ZipSync file

Uploads an EPIC ZipSync file to your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/upload-an-epic-zip-sync-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/upload-an-epic-zip-sync-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/upload-an-epic-zip-sync-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "by": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "processedCount": 1,
      "started": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totalCount": 1,
      "transform": {
        "name": "Ava Chen",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `by.firstName` | string |  |
| `by.id` | string |  |
| `by.lastName` | string |  |
| `by.links.self` | string |  |
| `by.recipientType` | string |  |
| `by.targetName` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `processedCount` | number |  |
| `started` | date |  |
| `status` | string |  |
| `totalCount` | number |  |
| `transform.name` | string |  |
| `transform.url` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST uploads/{uploadId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-an-epic-zip-sync-file.md) for the provider-specific parameters and requirements.

