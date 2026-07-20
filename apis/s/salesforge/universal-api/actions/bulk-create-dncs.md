# Salesforge: Bulk Create DNCs

Creates DNC entries in bulk in Salesforge.

```
POST https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/bulk-create-dncs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/bulk-create-dncs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
  "dncs[]": "dnc@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/bulk-create-dncs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
    "dncs[]": "dnc@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |
| `dncs[]` | array<string> | yes | Example: `dnc@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |

## Native endpoint

Through the native Salesforge API, this operation is `POST /public/v2/workspaces/:workspaceID/dnc/bulk` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-dncs.md) for the provider-specific parameters and requirements.

