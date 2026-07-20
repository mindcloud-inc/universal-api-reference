# ApproveThis: List Templates

Retrieves approval templates from your ApproveThis workspace.

```
GET https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allowAnonymousResponses": 1,
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
| `allowAnonymousResponses` | number |  |
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

Through the native ApproveThis API, this operation is `GET /templates` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

