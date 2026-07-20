# NiftyImages: Create ChatFuel Response Image

Creates a ChatFuel response image in NiftyImages.

```
POST https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/create-chat-fuel-response-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/create-chat-fuel-response-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/create-chat-fuel-response-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Url` | string | yes | NiftyImages URL that should be formatted. |
| `Variables[]` | array<object> | no | Variables array. |
| `Variables[].Name` | string | no | Variable or placeholder name. |
| `Variables[].Value` | string | no | Value appended to the final result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages[]` | array<object> |  |
| `messages[].attachment` | object |  |
| `messages[].attachment.payload` | object |  |
| `messages[].attachment.payload.url` | string |  |
| `messages[].attachment.type` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `POST /ChatFuel` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-fuel-response-image.md) for the provider-specific parameters and requirements.

