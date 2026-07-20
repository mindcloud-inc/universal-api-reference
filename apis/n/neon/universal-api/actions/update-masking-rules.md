# Neon: Update masking rules

Updates masking rules in Neon.

```
PUT https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-masking-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-masking-rules" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string",
  "masking_rules[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/update-masking-rules', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string",
    "masking_rules[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `masking_rules[]` | array<object> | yes | Neon API parameter masking_rules |

## Response

```json
{
  "success": true,
  "data": [
    {
      "masking_rules": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `masking_rules` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `PATCH /projects/:project_id/branches/:branch_id/masking_rules` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-masking-rules.md) for the provider-specific parameters and requirements.

