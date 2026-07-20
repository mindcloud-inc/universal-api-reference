# Paperform: List Forms

Retrieves forms from Paperform.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-forms?${params}`, {
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

Through the native Paperform API, this operation is `GET /forms` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

