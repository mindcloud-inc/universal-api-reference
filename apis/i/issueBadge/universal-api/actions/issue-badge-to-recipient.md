# IssueBadge: Issue Badge to Recipient



```
POST https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/issue-badge-to-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IssueBadge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/issue-badge-to-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "badgeId": "string",
  "name": "Ava Chen",
  "idempotencyKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/issue-badge-to-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "badgeId": "string",
    "name": "Ava Chen",
    "idempotencyKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badgeId` | string | yes | Encrypted badge ID from badge creation |
| `name` | string | yes | Recipient full name |
| `email` | string | no | Recipient email address |
| `phone` | string | no | Recipient phone number |
| `idempotencyKey` | string | yes | Unique key to prevent duplicate issuance |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Custom field values and additional metadata |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IssueId": "string",
      "publicUrl": "https://example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IssueId` | string | Encrypted issue ID for tracking |
| `publicUrl` | string | Public URL for badge verification |
| `success` | boolean | Whether the badge issuance succeeded |

## Native endpoint

Through the native IssueBadge API, this operation is `POST /issue/create` (base URL `https://app.issuebadge.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-badge-to-recipient.md) for the provider-specific parameters and requirements.

