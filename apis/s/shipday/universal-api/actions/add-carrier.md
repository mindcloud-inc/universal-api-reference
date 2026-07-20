# Shipday: Add Carrier

Creates a new carrier in Shipday.

```
POST https://connect.mindcloud.co/v1/universal/shipday/latest/actions/add-carrier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/add-carrier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipday/latest/actions/add-carrier', {
  method: 'POST',
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
| `name` | string | no | Full name of the carrier. Example: `John Doe`. |
| `email` | string | no | Email address for the carrier. Example: `user@example.com`. |
| `phoneNumber` | string | no | Phone number for the carrier. Example: `+1-555-123-4567`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shipday API returns.

## Native endpoint

Through the native Shipday API, this operation is `POST /carriers` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-carrier.md) for the provider-specific parameters and requirements.

