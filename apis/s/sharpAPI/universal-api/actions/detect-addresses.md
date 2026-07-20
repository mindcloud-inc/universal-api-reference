# SharpAPI: Detect Addresses

Creates an address detection job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/detect-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/detect-addresses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Ship the order to 1600 Amphitheatre Parkway, Mountain View, CA 94043, United States."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/detect-addresses', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Ship the order to 1600 Amphitheatre Parkway, Mountain View, CA 94043, United States."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Provide the content from where address information needs to be detected. Example: `Ship the order to 1600 Amphitheatre Parkway, Mountain View, CA 94043, United States.`. |

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

Through the native SharpAPI API, this operation is `POST /content/detect_address` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-addresses.md) for the provider-specific parameters and requirements.

