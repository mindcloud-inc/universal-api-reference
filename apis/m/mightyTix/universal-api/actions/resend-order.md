# Mighty Tix: Resend Order

Resends an order in Mighty Tix.

```
PUT https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/resend-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/resend-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/resend-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.id` | string | yes | Order ID from the Mighty Tix Admin GraphQL docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resendOrder": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resendOrder` | boolean |  |

## Native endpoint

Through the native Mighty Tix API, this operation is `POST admin-api/graphql` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-order.md) for the provider-specific parameters and requirements.

