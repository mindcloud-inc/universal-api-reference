# smapOne: Get account

Retrieves the current account from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-account?${params}`, {
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
      "availableFeatures": [
        "string"
      ],
      "companyName": "Ava Chen",
      "email": "ava@example.com",
      "roles": [
        "string"
      ],
      "subscriptionId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableFeatures` | array<string> |  |
| `companyName` | string |  |
| `email` | string |  |
| `roles` | array<string> |  |
| `subscriptionId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /intern/Account` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

