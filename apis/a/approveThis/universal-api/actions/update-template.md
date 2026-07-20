# ApproveThis: Update Template

Updates an existing approval template in ApproveThis.

```
PUT https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template": "mindcloud-template-probe",
  "name": "Ava Chen",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template": "mindcloud-template-probe",
    "name": "Ava Chen",
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | string | yes | The template slug. Example: `mindcloud-template-probe`. |
| `name` | string | yes | The template name. |
| `slug` | string | yes | A unique template slug. |
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

Through the native ApproveThis API, this operation is `PUT /templates/:template` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

