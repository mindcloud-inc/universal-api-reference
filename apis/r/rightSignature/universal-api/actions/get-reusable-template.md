# RightSignature: Get Reusable Template

Retrieves a specific reusable template from RightSignature.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-reusable-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-reusable-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-reusable-template?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Reusable Template ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {},
      "distributionMethod": "string",
      "expiresIn": 1,
      "filename": "Ava Chen",
      "id": "string",
      "identityMethod": "string",
      "kba": true,
      "mergeFieldComponents": [
        "string"
      ],
      "name": "Ava Chen",
      "pageImageUrls": [
        "https://example.com"
      ],
      "passcode": true,
      "roles": [
        {}
      ],
      "sharedWith": [
        "string"
      ],
      "signerSequencing": true,
      "tags": {},
      "thumbnailUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `creator` | object |  |
| `distributionMethod` | string |  |
| `expiresIn` | number |  |
| `filename` | string |  |
| `id` | string |  |
| `identityMethod` | string |  |
| `kba` | boolean |  |
| `mergeFieldComponents` | array<string> |  |
| `name` | string |  |
| `pageImageUrls` | array<string> |  |
| `passcode` | boolean |  |
| `roles` | array<object> |  |
| `sharedWith` | array<string> |  |
| `signerSequencing` | boolean |  |
| `tags` | object |  |
| `thumbnailUrl` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET /reusable_templates/:id` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reusable-template.md) for the provider-specific parameters and requirements.

