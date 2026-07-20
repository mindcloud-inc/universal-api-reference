# Devin: Replace Session Tags

Updates session tags by replacing them in Devin.

```
PUT https://connect.mindcloud.co/v1/universal/devin/latest/actions/replace-session-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/devin/latest/actions/replace-session-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "devinId": "string",
  "orgId": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/replace-session-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "devinId": "string",
    "orgId": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `devinId` | string | yes | Session ID prefixed with devin-. |
| `orgId` | string | yes | Devin organization ID. |
| `tags[]` | array<string> | yes | Replacement tag list for the session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags` | array<string> | Tags assigned to the session after replacement. |

## Native endpoint

Through the native Devin API, this operation is `PUT /v3/organizations/:org_id/sessions/:devin_id/tags` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-session-tags.md) for the provider-specific parameters and requirements.

