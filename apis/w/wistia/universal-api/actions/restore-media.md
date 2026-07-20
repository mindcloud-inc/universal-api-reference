# Wistia: Restore Media

Restores archived media to your Wistia account.

```
PUT https://connect.mindcloud.co/v1/universal/wistia/latest/actions/restore-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/restore-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaHashedIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wistia/latest/actions/restore-media', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaHashedIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaHashedIds[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundJobStatus": {
        "id": 1,
        "status": "string"
      },
      "container": {
        "hashedId": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundJobStatus` | object | A background job keeps track of the progress of an asynchronous task, e.g bulk archiving media, translating media, etc. |
| `backgroundJobStatus.id` | number | The ID of the background job that's been queued for the request. |
| `backgroundJobStatus.status` | string | The status of the background job that's been queued for the request. |
| `container` | object |  |
| `container.hashedId` | string | The hashed ID of the container the medias will be restored to. |
| `container.name` | string | The display name of the container the medias will be restored to. |
| `container.type` | string | The type of container the medias will be restored to. |
| `message` | string | A confirmation message that the background job has been queued. |

## Native endpoint

Through the native Wistia API, this operation is `PUT /modern/medias/restore` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-media.md) for the provider-specific parameters and requirements.

