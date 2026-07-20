# ClassDo: Start Recording

Updates a recording to started in ClassDo.

```
PUT https://connect.mindcloud.co/v1/universal/classDo/latest/actions/start-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/start-recording" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation StartRecording { startRecording(data: { roomId: \"ROOM_ID\" }) { id status } }"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classDo/latest/actions/start-recording', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation StartRecording { startRecording(data: { roomId: \"ROOM_ID\" }) { id status } }"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation payload. Default: `mutation StartRecording { startRecording(data: { roomId: \"ROOM_ID\" }) { id status } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "startRecording": {
          "id": "string",
          "status": "string"
        }
      },
      "errors": [
        {
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.startRecording.id` | string |  |
| `data.startRecording.status` | string |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-recording.md) for the provider-specific parameters and requirements.

