# ApproveThis: Create Template

Creates a new approval template in ApproveThis.

```
POST https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Quarterly Budget Request",
  "slug": "quarterly-budget-request"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Quarterly Budget Request",
    "slug": "quarterly-budget-request"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The template name. Example: `Quarterly Budget Request`. |
| `slug` | string | yes | A unique template slug. Example: `quarterly-budget-request`. |
| `description` | string | no | An optional template description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowAnonymousResponses": true,
      "createdAt": "string",
      "description": "string",
      "id": 1,
      "isActive": true,
      "name": "Ava Chen",
      "ownerId": "string",
      "ownerType": "string",
      "settings": {
        "allowResubmissions": true,
        "commentsEnabled": true,
        "commentsImmutable": true,
        "loginForApprovers": true,
        "maxResubmissions": {},
        "signedUrlExpirationDays": 1,
        "signedUrlsEnabled": true
      },
      "slug": "string",
      "teamId": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowAnonymousResponses` | boolean |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `ownerId` | string |  |
| `ownerType` | string |  |
| `settings.allowResubmissions` | boolean |  |
| `settings.commentsEnabled` | boolean |  |
| `settings.commentsImmutable` | boolean |  |
| `settings.loginForApprovers` | boolean |  |
| `settings.maxResubmissions` | object |  |
| `settings.signedUrlExpirationDays` | number |  |
| `settings.signedUrlsEnabled` | boolean |  |
| `slug` | string |  |
| `teamId` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native ApproveThis API, this operation is `POST /templates` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

