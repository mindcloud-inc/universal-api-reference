# Jetbuilt: Create Project



```
POST https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "userId": "string",
  "name": "Ava Chen",
  "locationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "userId": "string",
    "name": "Ava Chen",
    "locationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budget` | string | no |  |
| `city` | string | no |  |
| `clientId` | string | yes |  |
| `closeDate` | string | no |  |
| `contractNumber` | string | no |  |
| `country` | string | no |  |
| `currency` | string | no |  |
| `customId` | string | no |  |
| `paidToDate` | string | no |  |
| `priceValidUntil` | string | no |  |
| `primaryContactId` | string | no |  |
| `probability` | string | no |  |
| `projectType` | string | no |  |
| `shortDescription` | string | no |  |
| `state` | string | no |  |
| `streetAddress` | string | no |  |
| `tax` | string | no |  |
| `userId` | string | yes |  |
| `zipCode` | string | no |  |
| `name` | string | yes |  |
| `locationId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `POST projects` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

