# Scalr: Update Access Token

Updates an existing access token in Scalr.

```
PUT https://connect.mindcloud.co/v1/universal/scalr/latest/actions/update-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scalr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scalr/latest/actions/update-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "access_token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scalr/latest/actions/update-access-token', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "access_token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access_token` | string | yes | Scalr access token ID. |
| `data.attributes.name` | string | no | Access token name. |
| `data.attributes.description` | string | no | Access token description. |
| `data.attributes.expires-in` | number | no | Minutes until the token expires. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scalr API returns.

## Native endpoint

Through the native Scalr API, this operation is `PATCH /access-tokens/:access_token` (base URL `https://mindcloud.scalr.io/api/iacp/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-access-token.md) for the provider-specific parameters and requirements.

