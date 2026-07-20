# Kommunicate: Update User Details

Updates an existing user in Kommunicate.

```
PUT https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/update-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/update-user-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ofUserId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/update-user-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ofUserId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ofUserId` | string | yes | User ID to route into the required Of-User-Id header. |
| `email` | string | no | Updated email address for the user. |
| `displayName` | string | no | Updated display name for the user. |
| `imageLink` | string | no | Updated profile image URL for the user. |
| `metadata` | object | no | Optional user metadata fields visible in the dashboard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generatedAt": 1,
      "response": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generatedAt` | number | Provider-generated timestamp. |
| `response` | string | Provider response message. |
| `status` | string | Provider operation status. |

## Native endpoint

Through the native Kommunicate API, this operation is `POST /rest/ws/user/update` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-details.md) for the provider-specific parameters and requirements.

