# RICOH360 Tours: Update Virtual Business Card



```
PUT https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/update-virtual-business-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RICOH360 Tours `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/update-virtual-business-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/update-virtual-business-card', {
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
| `description` | string | no | Business-card style description content. |
| `tourId` | string | no | Tour ID to update business-card content for. |
| `tourName` | string | no | Tour name to keep on the updated tour. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RICOH360 Tours API returns.

## Native endpoint

Through the native RICOH360 Tours API, this operation is `POST /graphql` (base URL `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-virtual-business-card.md) for the provider-specific parameters and requirements.

