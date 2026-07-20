# OnePageCRM: List Users

Retrieves users from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-users?${params}`, {
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
      "accountRights": [
        "string"
      ],
      "accountRole": "string",
      "bccEmail": "ava@example.com",
      "companyName": "Ava Chen",
      "countryCode": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "googleContactsEmail": {},
      "id": "string",
      "lastName": "Chen",
      "photoUrl": "https://example.com",
      "virtualGroupId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountRights[]` | string |  |
| `accountRole` | string |  |
| `bccEmail` | string |  |
| `companyName` | string |  |
| `countryCode` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `googleContactsEmail` | object |  |
| `id` | string |  |
| `lastName` | string |  |
| `photoUrl` | string |  |
| `virtualGroupId` | string |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /users` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

