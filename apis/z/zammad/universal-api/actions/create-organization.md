# Zammad: Create Organization

Creates a new organization in Zammad.

```
POST https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MC TEST ORG"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MC TEST ORG"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Organization name. Example: `MC TEST ORG`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zammad API returns.

## Native endpoint

Through the native Zammad API, this operation is `POST /organizations` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization.md) for the provider-specific parameters and requirements.

