# Routee: Track an Email Validator request

Tracks an email validator request in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-an-email-validator-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-an-email-validator-request?connectionId=$CONNECTION_ID&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-an-email-validator-request?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackingId` | string | yes | The unique tracking id of the Email Validation request to track |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "details": {
        "exists": true,
        "hasValidDNS": true,
        "hasValidFormat": true
      },
      "email": "ava@example.com",
      "label": "string",
      "price": 1,
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `details` | object |  |
| `details.exists` | boolean |  |
| `details.hasValidDNS` | boolean |  |
| `details.hasValidFormat` | boolean |  |
| `email` | string |  |
| `label` | string |  |
| `price` | number |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /emailvalidator/tracking/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-an-email-validator-request.md) for the provider-specific parameters and requirements.

