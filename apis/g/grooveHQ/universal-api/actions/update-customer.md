# GrooveHQ: Update Customer

Updates an existing customer in GrooveHQ.

```
PUT https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerEmail": "customer@example.com",
  "email": "customer@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerEmail": "customer@example.com",
    "email": "customer@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerEmail` | string | yes | Example: `customer@example.com`. |
| `email` | string | yes | Example: `customer@example.com`. |
| `name` | string | no | Example: `Jamie Customer`. |
| `about` | string | no | Example: `Important account contact`. |
| `twitterUsername` | string | no | Example: `grooveuser`. |
| `title` | string | no | Example: `Support Lead`. |
| `companyName` | string | no | Example: `MindCloud`. |
| `phoneNumber` | string | no | Example: `+1 555 123 4567`. |
| `location` | string | no | Example: `Remote`. |
| `linkedinUsername` | string | no | Example: `jamie-customer`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrooveHQ API returns.

## Native endpoint

Through the native GrooveHQ API, this operation is `PUT /customers/:customerEmail` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

