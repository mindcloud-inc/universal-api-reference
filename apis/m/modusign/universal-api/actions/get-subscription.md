# Modusign: Get Subscription

Retrieves current subscription details from Modusign.

```
GET https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-subscription?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "isSubscribing": true,
      "nextResetDate": "2026-05-07T12:00:00.000Z",
      "plan": {},
      "resetDateOfMonth": 1,
      "status": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSubscribing` | boolean |  |
| `nextResetDate` | date |  |
| `plan` | object |  |
| `resetDateOfMonth` | number |  |
| `status` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Modusign API, this operation is `GET /subscription` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

