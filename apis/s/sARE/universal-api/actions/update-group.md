# SARE: Update Group

Updates an existing group in SARE.

```
PUT https://connect.mindcloud.co/v1/universal/sARE/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SARE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groups[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sARE/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groups[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groups[]` | array<object> | yes | Array of group objects to send to the SARE update-group route. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SARE API returns.

## Native endpoint

Through the native SARE API, this operation is `POST /group/edit` (base URL `https://s.enewsletter.pl/api/v1/{{credentials.uid}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

