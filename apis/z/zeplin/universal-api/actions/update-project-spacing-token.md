# Zeplin: Update Project Spacing Token

Updates an existing project spacing token in Zeplin.

```
PUT https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-spacing-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-spacing-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "spacingTokenId": "string",
  "name": "Ava Chen",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-spacing-token', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "spacingTokenId": "string",
    "name": "Ava Chen",
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project id |
| `spacingTokenId` | string | yes | Spacing token id |
| `name` | string | yes | The name of the token |
| `value` | number | yes | The value of the token |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeplin API returns.

## Native endpoint

Through the native Zeplin API, this operation is `PATCH /projects/{project_id}/spacing_tokens/{spacing_token_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-spacing-token.md) for the provider-specific parameters and requirements.

