# SMS.to: Estimate Single Message Legacy GET

Retrieves a cost estimate for a single SMS message using SMS.to's legacy endpoint.

```
GET https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/estimate-single-message-legacy-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/estimate-single-message-legacy-get?connectionId=$CONNECTION_ID&message=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "message": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/estimate-single-message-legacy-get?${params}`, {
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
| `message` | string | yes | Your message. |
| `to` | string | yes | Phone number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderId` | string | no | The displayed value of who sent the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactCount": 1,
      "estimatedCost": 1,
      "invalidCount": 1,
      "smsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactCount` | number |  |
| `estimatedCost` | number |  |
| `invalidCount` | number |  |
| `smsCount` | number |  |

## Native endpoint

Through the native SMS.to API, this operation is `GET /sms/estimate` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-single-message-legacy-get.md) for the provider-specific parameters and requirements.

