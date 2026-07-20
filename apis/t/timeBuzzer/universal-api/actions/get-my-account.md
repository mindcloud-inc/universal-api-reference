# timeBuzzer: Get My Account



```
GET https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/get-my-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/get-my-account?${params}`, {
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
      "accountId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "permissions": [
        "string"
      ],
      "state": "string",
      "templateId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Identifier of the authenticated user's timeBuzzer account. |
| `email` | string | Email address of the authenticated timeBuzzer user. |
| `firstName` | string | First name of the authenticated timeBuzzer user. |
| `id` | number | Unique identifier of the authenticated timeBuzzer user. |
| `lastName` | string | Last name of the authenticated timeBuzzer user. |
| `permissions` | array<string> | Permissions granted to the authenticated timeBuzzer user. |
| `state` | string | Current state of the authenticated timeBuzzer user. |
| `templateId` | number | Identifier of the template assigned to the authenticated user. |

## Native endpoint

Through the native timeBuzzer API, this operation is `GET /open-api/account/me` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-account.md) for the provider-specific parameters and requirements.

