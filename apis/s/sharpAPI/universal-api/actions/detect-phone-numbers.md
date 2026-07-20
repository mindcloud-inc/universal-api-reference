# SharpAPI: Detect Phone Numbers

Creates a phone number detection job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/detect-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/detect-phone-numbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Call: 1800-394-7486 or our Singapore office +65 8888 8888"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/detect-phone-numbers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Call: 1800-394-7486 or our Singapore office +65 8888 8888"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Provide the content from where the mobile number needs to be detected. Example: `Call: 1800-394-7486 or our Singapore office +65 8888 8888`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Provider job identifier for the submitted AI job. |
| `statusUrl` | string | Provider status URL for polling the AI job result. |

## Native endpoint

Through the native SharpAPI API, this operation is `POST /content/detect_phones` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-phone-numbers.md) for the provider-specific parameters and requirements.

