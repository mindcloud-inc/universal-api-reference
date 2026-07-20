# Rebrandly: Delete Link

Deletes an existing link from Rebrandly.

```
DELETE https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-link?connectionId=$CONNECTION_ID&id=3f45c115e8e349f0b6a8e193693b7cda" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "3f45c115e8e349f0b6a8e193693b7cda"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-link?${params}`, {
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
| `id` | string | yes | Unique identifier of the branded short link to delete. Example: `3f45c115e8e349f0b6a8e193693b7cda`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {},
      "destination": "string",
      "domain": {},
      "domainId": "string",
      "domainName": "Ava Chen",
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "favourite": true,
      "https": true,
      "id": "string",
      "integrated": true,
      "isPublic": true,
      "linkType": "https://example.com",
      "shortUrl": "https://example.com",
      "slashtag": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number | Click count. |
| `createdAt` | date | Created timestamp. |
| `creator` | object | Creator details. |
| `destination` | string | Destination URL. |
| `domain` | object | Domain details. |
| `domainId` | string | Domain ID. |
| `domainName` | string | Domain name. |
| `expiredAt` | date | Expiration timestamp, if any. |
| `favourite` | boolean | Favourite flag. |
| `https` | boolean | Whether HTTPS is enabled. |
| `id` | string | Link ID. |
| `integrated` | boolean | Whether the link is integrated. |
| `isPublic` | boolean | Whether the link is public. |
| `linkType` | string | Link type. |
| `shortUrl` | string | Short URL. |
| `slashtag` | string | Keyword portion of the short URL. |
| `status` | string | Link status. |
| `tags` | array<object> | Attached tags. |
| `title` | string | Link title. |
| `updatedAt` | date | Last updated timestamp. |

## Native endpoint

Through the native Rebrandly API, this operation is `DELETE /links/:id` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-link.md) for the provider-specific parameters and requirements.

