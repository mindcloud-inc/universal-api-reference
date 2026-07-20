# CloudContactAI: Patch Client by ID



```
PUT https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/patch-client-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/patch-client-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/patch-client-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | The client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "accountName": "Ava Chen",
      "country": "string",
      "id": 1,
      "incomingSmsCC": "string",
      "incomingSmsMainEmail": true,
      "name": "Ava Chen",
      "notifyIncomingSms": true,
      "smsLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `accountName` | string |  |
| `country` | string |  |
| `id` | number |  |
| `incomingSmsCC` | string |  |
| `incomingSmsMainEmail` | boolean |  |
| `name` | string |  |
| `notifyIncomingSms` | boolean |  |
| `smsLimit` | number |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `PATCH api/clients/:id` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-client-by-id.md) for the provider-specific parameters and requirements.

