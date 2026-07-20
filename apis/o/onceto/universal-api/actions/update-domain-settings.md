# Once.to: Update Domain Settings

Updates an existing domain in Once.to.

```
PUT https://connect.mindcloud.co/v1/universal/onceto/latest/actions/update-domain-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Once.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onceto/latest/actions/update-domain-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "domain-id",
  "name": "go.example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceto/latest/actions/update-domain-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "domain-id",
    "name": "go.example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the domain to update. Example: `domain-id`. |
| `name` | string | yes | Existing domain name. Once.to requires it to remain unchanged. Example: `go.example.com`. |
| `description` | string | no | Optional remarks for the domain. Example: `MindCloud managed domain`. |
| `rootRedirUrl` | string | no | Optional redirect URL for the domain root. Example: `https://example.com`. |
| `notFoundRedirUrl` | string | no | Optional redirect URL when a slug is not found. Example: `https://example.com/404`. |
| `default` | boolean | no | Whether to make this domain the default. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Once.to API returns.

## Native endpoint

Through the native Once.to API, this operation is `PUT /domains/:id` (base URL `https://once.to/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain-settings.md) for the provider-specific parameters and requirements.

