# ChurchStamp: Get User Details

Retrieves authenticated user details from ChurchStamp.

```
GET https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChurchStamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-user-details?${params}`, {
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
      "creditsBalance": {},
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "subscriptionPlan": "string",
      "subscriptionStatus": "string",
      "vAddress": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsBalance` | object |  |
| `emailAddress` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `subscriptionPlan` | string |  |
| `subscriptionStatus` | string |  |
| `vAddress` | object |  |

## Native endpoint

Through the native ChurchStamp API, this operation is `GET /get-user` (base URL `https://v2.churchstamp.com/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

