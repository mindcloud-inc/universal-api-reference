# Shotstack: Render Template



```
POST https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/render-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/render-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/render-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The Shotstack request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "response": {
        "id": "string",
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Status message returned by Shotstack. |
| `response.id` | string | Queued render identifier. |
| `response.message` | string | Render queue confirmation message. |
| `success` | boolean | Whether the template render request succeeded. |

## Native endpoint

Through the native Shotstack API, this operation is `POST /edit/v1/templates/render` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-template.md) for the provider-specific parameters and requirements.

