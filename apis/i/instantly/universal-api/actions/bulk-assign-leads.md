# Instantly: Bulk Assign Leads

Assigns leads to users in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/bulk-assign-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/bulk-assign-leads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationUserIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/bulk-assign-leads', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationUserIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationUserIds[]` | array<string> | yes | Organization user IDs to assign matching leads to. |
| `ids[]` | array<string> | no | Lead IDs to assign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/leads/bulk-assign` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-assign-leads.md) for the provider-specific parameters and requirements.

