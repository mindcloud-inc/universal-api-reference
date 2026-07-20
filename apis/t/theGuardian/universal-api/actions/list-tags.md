# The Guardian: List Tags

Finds matching tags in The Guardian.

```
GET https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Guardian `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-tags?${params}`, {
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
| `q` | string | no | Return tags containing exactly this free text. |
| `reference` | string | no | Filter tags by reference value. |
| `referenceType` | string | no | Filter tags by reference type. |
| `section` | string | no | Filter tags to one or more sections. |
| `showReferences` | string | no | Comma-separated reference groups to include in each tag result. |
| `type` | string | no | Filter tags by type. |
| `webTitle` | string | no | Return tags whose web title starts with this prefix. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "bio": "string",
      "description": "string",
      "firstName": "Ava",
      "id": "string",
      "keywordType": "string",
      "lastName": "Chen",
      "sectionId": "string",
      "sectionName": "Ava Chen",
      "type": "string",
      "webTitle": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `bio` | string |  |
| `description` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `keywordType` | string |  |
| `lastName` | string |  |
| `sectionId` | string |  |
| `sectionName` | string |  |
| `type` | string |  |
| `webTitle` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native The Guardian API, this operation is `GET /tags` (base URL `https://content.guardianapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

