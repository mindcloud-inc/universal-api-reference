# Adrapid: Create User Template

Creates a new template for a user in Adrapid.

```
POST https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/create-user-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adrapid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/create-user-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adrapid/latest/actions/create-user-template', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adrapid API returns.

## Native endpoint

Through the native Adrapid API, this operation is `POST /users/:userId/templates` (base URL `https://api.adrapid.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-template.md) for the provider-specific parameters and requirements.

