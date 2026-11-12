# Jobber: Edit Client



```
PUT https://connect.mindcloud.co/v1/universal/jobber/latest/actions/edit-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/edit-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jobber/latest/actions/edit-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Jobber client ID to update. |
| `customFields` | string | no | Optional JSON array of Jobber custom field edits. Example: `[{"customFieldConfigurationId":"...","valueText":"..."}]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jobber API returns.

## Native endpoint

Through the native Jobber API, this operation is `POST graphql` (base URL `https://api.getjobber.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-client.md) for the provider-specific parameters and requirements.

