# Webling: Create Membergroup



```
POST https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-membergroup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-membergroup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Stage 3 Member Group"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-membergroup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Stage 3 Member Group"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title for the new member group. Example: `Stage 3 Member Group`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Webling API returns.

## Native endpoint

Through the native Webling API, this operation is `POST /membergroup` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-membergroup.md) for the provider-specific parameters and requirements.

