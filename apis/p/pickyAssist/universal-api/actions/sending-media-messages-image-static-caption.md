# Picky Assist: Sending Media Messages - Image Static Caption



```
POST https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/sending-media-messages-image-static-caption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/sending-media-messages-image-static-caption" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "application": "string",
  "globalmessage": "string",
  "globalmedia": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/sending-media-messages-image-static-caption', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "application": "string",
    "globalmessage": "string",
    "globalmedia": "string",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `application` | string | yes |  |
| `globalmessage` | string | yes |  |
| `globalmedia` | string | yes |  |
| `data[]` | array<object> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `priority` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "credit": "string",
          "msg_id": "string",
          "number": "string"
        }
      ],
      "message": "string",
      "push_id": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].credit` | string |  |
| `data[].msg_id` | string |  |
| `data[].number` | string |  |
| `message` | string |  |
| `push_id` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /push` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sending-media-messages-image-static-caption.md) for the provider-specific parameters and requirements.

