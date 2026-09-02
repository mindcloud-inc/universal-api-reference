# Jetbuilt: Update Client



```
PUT https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/update-client', {
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
| `externalIds` | object | no | Use this object to associate any other Id |
| `id` | number | no |  |
| `city` | string | no |  |
| `country` | string | no |  |
| `description` | string | no |  |
| `parentId` | string | no |  |
| `phone` | string | no |  |
| `state` | string | no |  |
| `streetAddress` | string | no |  |
| `userId` | string | no |  |
| `website` | string | no |  |
| `zipCode` | string | no |  |
| `companyName` | string | no |  |
| `owner.id` | string | no |  |
| `owner.name` | string | no |  |
| `metadata` | object | no |  |
| `owner` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `PATCH clients/:id` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

