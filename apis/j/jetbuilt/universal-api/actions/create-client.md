# Jetbuilt: Create Client



```
POST https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-client', {
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
| `city` | string | no | Example: `San Francisco`. |
| `country` | string | no | Example: `United States`. |
| `description` | string | no | Example: `Quarterly onboarding package`. |
| `parentId` | string | no | Example: `parent_01J1KR2F8G5`. |
| `phone` | string | no | Example: `+1 415 555 0132`. |
| `state` | string | no | Example: `California`. |
| `streetAddress` | string | no | Example: `100 Market St`. |
| `userId` | string | no | Example: `usr_01HZX3Q8N7A2`. |
| `website` | string | no | Example: `https://acme.example`. |
| `zipCode` | string | no | Example: `94105`. |
| `companyName` | string | no | Example: `Acme Logistics`. |
| `owner.id` | string | no |  |
| `owner.name` | string | no |  |
| `metadata` | object | no |  |
| `owner` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `POST clients` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

