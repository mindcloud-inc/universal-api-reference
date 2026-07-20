# GatherUp: Reply to Customer

Creates a reply to a customer in GatherUp.

```
POST https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/reply-to-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/reply-to-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/reply-to-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Customer id. |
| `content` | string | yes | The content of the comment. |
| `title` | string | no | Your title. |
| `visibility` | number | no | The visibility the response. Is response public? (1 - yes, 0 - no) |
| `respondAsBusinessOwner` | number | no | Respond as business owner (otherwise response will be from logged in user, 1 - yes, 0 - no) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /customer/reply` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-customer.md) for the provider-specific parameters and requirements.

