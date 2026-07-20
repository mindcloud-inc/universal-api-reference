# Rebrandly: List Links

Retrieves links from Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/list-links?${params}`, {
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
| `limit` | number | no | Maximum number of links to return. Example: `25`. |
| `favourite` | boolean | no | Filter links by favourite status. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain.id` | string | no | Filter links by branded domain ID. Example: `8f104cc5b6ee4a4ba7897b06ac2ddcfb`. |
| `domain.fullName` | string | no | Filter links by branded domain name. Example: `rebrand.ly`. |
| `creator.id` | string | no | Filter links by creator ID. Example: `6f549f0a64b74f69952e71c1727dc9a9`. |
| `slashtag` | string | no | Filter links by slashtag. Requires a domain filter in Rebrandly docs. Example: `mc0422155153`. |
| `dateFrom` | date | no | Include only links created on or after this date (YYYY-MM-DD). Example: `2026-04-22`. |
| `dateTo` | date | no | Include only links created on or before this date (YYYY-MM-DD). Example: `2026-04-22`. |
| `orderBy` | string | no | Field used to sort the links collection. Example: `createdAt`. |
| `orderDir` | string | no | Sort direction for the links collection. Example: `desc`. |
| `last` | string | no | Cursor: the last link ID returned by the previous page. Example: `3f45c115e8e349f0b6a8e193693b7cda`. |

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

Through the native Rebrandly API, this operation is `GET /links` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

