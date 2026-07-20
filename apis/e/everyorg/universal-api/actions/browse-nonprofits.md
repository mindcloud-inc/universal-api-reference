# Every.org: Browse Nonprofits

Finds nonprofits in Every.org by cause.

```
GET https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/browse-nonprofits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Every.org `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/browse-nonprofits?connectionId=$CONNECTION_ID&limit=25&offset=0&cause=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "cause": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/browse-nonprofits?${params}`, {
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
| `cause` | string | yes | Cause slug to browse. |
| `take` | number | no | Results per page. Maximum 100. |
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coverImageUrl": "https://example.com",
      "description": "string",
      "donationsEnabled": true,
      "hasAdmin": true,
      "location": "string",
      "logoCloudinaryId": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "profileUrl": "https://example.com",
      "slug": "string",
      "tags": [
        "string"
      ],
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverImageUrl` | string |  |
| `description` | string |  |
| `donationsEnabled` | boolean |  |
| `hasAdmin` | boolean |  |
| `location` | string |  |
| `logoCloudinaryId` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `profileUrl` | string |  |
| `slug` | string |  |
| `tags[]` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Every.org API, this operation is `GET /browse/:cause` (base URL `https://partners.every.org/v0.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/browse-nonprofits.md) for the provider-specific parameters and requirements.

