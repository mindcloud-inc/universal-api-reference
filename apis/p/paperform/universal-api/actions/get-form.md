# Paperform: Get Form

Retrieves a form from Paperform.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form?connectionId=$CONNECTION_ID&slugOrId=contact-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slugOrId": "contact-form"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/get-form?${params}`, {
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
| `slugOrId` | list<string> | yes | Paperform form slug or numeric ID. Example: `contact-form`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTimezone": "string",
      "additionalUrls": {
        "duplicateUrl": "https://example.com",
        "editUrl": "https://example.com",
        "submissionsUrl": "https://example.com"
      },
      "coverImageUrl": "https://example.com",
      "createdAt": "string",
      "createdAtUtc": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "live": true,
      "slug": "string",
      "spaceId": 1,
      "submissionCount": 1,
      "title": "string",
      "updatedAt": "string",
      "updatedAtUtc": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTimezone` | string |  |
| `additionalUrls` | object |  |
| `additionalUrls.duplicateUrl` | string |  |
| `additionalUrls.editUrl` | string |  |
| `additionalUrls.submissionsUrl` | string |  |
| `coverImageUrl` | string |  |
| `createdAt` | string |  |
| `createdAtUtc` | date |  |
| `description` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `slug` | string |  |
| `spaceId` | number |  |
| `submissionCount` | number |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updatedAtUtc` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

