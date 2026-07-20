# Salesflare: Update Account



```
PUT https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Salesflare account ID. |
| `name` | string | no | The account name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Salesflare API, this operation is `PUT accounts/:account_id` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

