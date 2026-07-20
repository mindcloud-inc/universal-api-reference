# Routee: Confirm a verification by its ID

Confirms a verification by its ID in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/confirm-a-verification-by-its-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/confirm-a-verification-by-its-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingId": "string",
  "answer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/confirm-a-verification-by-its-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackingId": "string",
    "answer": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackingId` | string | yes | the tracking id of the verification. |
| `answer` | number | yes | The answer of the verification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "string",
      "maxRetries": 1,
      "status": "string",
      "timesTried": 1,
      "trackingId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | string |  |
| `maxRetries` | number |  |
| `status` | string |  |
| `timesTried` | number |  |
| `trackingId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /2step/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-a-verification-by-its-id.md) for the provider-specific parameters and requirements.

