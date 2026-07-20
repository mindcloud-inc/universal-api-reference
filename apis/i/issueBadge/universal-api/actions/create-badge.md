# IssueBadge: Create Badge



```
POST https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/create-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IssueBadge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/create-badge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "badge_logo": "string",
  "issuingOrganizationName": "Ava Chen",
  "idempotencyKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/create-badge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "badge_logo": "string",
    "issuingOrganizationName": "Ava Chen",
    "idempotencyKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Badge name |
| `description` | string | yes | Badge description |
| `badge_logo` | file | yes | Badge logo image file |
| `issuingOrganizationName` | string | yes | Name of the issuing organization |
| `idempotencyKey` | string | yes | Unique key to prevent duplicate badge creation |
| `nickname` | string | no | Optional badge nickname |
| `leftPanelDescription` | string | no | Additional description for the left panel |
| `organizationId` | string | no | Existing organization ID |
| `comment` | string | no | Additional comments |
| `expireDate` | date | no | Badge expiration date |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields[]` | array<object> | no | Custom fields for this badge |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeId": "string",
      "organizationId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeId` | string | UUID of the created badge |
| `organizationId` | string | UUID of the organization |
| `success` | boolean | Whether the badge was created successfully |

## Native endpoint

Through the native IssueBadge API, this operation is `POST /badge/create` (base URL `https://app.issuebadge.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-badge.md) for the provider-specific parameters and requirements.

