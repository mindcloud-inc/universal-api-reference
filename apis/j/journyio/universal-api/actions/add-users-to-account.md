# Journy.io: Add Users to Account



```
PUT https://connect.mindcloud.co/v1/universal/journyio/latest/actions/add-users-to-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Journy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/add-users-to-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/journyio/latest/actions/add-users-to-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account.accountId` | string | no | Unique identifier for the account in your database. |
| `account.domain` | string | no | The domain associated with the account. |
| `users[]` | array<object> | yes | Users to add to the account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "meta": {
        "requestId": "string",
        "status": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `meta.requestId` | string |  |
| `meta.status` | number |  |

## Native endpoint

Through the native Journy.io API, this operation is `POST /accounts/users/add` (base URL `https://api.journy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-users-to-account.md) for the provider-specific parameters and requirements.

