# Instantly: Update Account

Updates an existing account in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email of the account. |
| `firstName` | string | no | First name associated with the account. |
| `lastName` | string | no | Last name associated with the account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address. |
| `first_name` | string | First name. |
| `last_name` | string | Last name. |
| `status` | number | Account status. |

## Native endpoint

Through the native Instantly API, this operation is `PATCH /api/v2/accounts/:email` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

