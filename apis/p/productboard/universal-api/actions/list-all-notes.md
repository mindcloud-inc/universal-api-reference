# Productboard: List All Notes

Retrieves notes from your Productboard workspace.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-notes?${params}`, {
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
      "company": {},
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "displayUrl": "https://example.com",
      "externalDisplayUrl": "https://example.com",
      "features": [
        {}
      ],
      "followers": [
        {}
      ],
      "id": "string",
      "owner": {},
      "source": {},
      "state": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object | Referenced company object. |
| `content` | string | Rich-text or HTML note content. |
| `createdAt` | date | Creation timestamp. |
| `createdBy` | object | Creator information. |
| `displayUrl` | string | Productboard URL for the note. |
| `externalDisplayUrl` | string | External source URL when present. |
| `features` | array<object> | Referenced features linked to the note. |
| `followers` | array<object> | Followers for the note. |
| `id` | string | Productboard note identifier. |
| `owner` | object | Owner information. |
| `source` | object | Source metadata. |
| `state` | string | Note processing state. |
| `tags` | array<string> | Tags applied to the note. |
| `title` | string | Note title. |
| `updatedAt` | date | Last update timestamp. |
| `user` | object | Referenced user object when present. |

## Native endpoint

Through the native Productboard API, this operation is `GET /notes` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-notes.md) for the provider-specific parameters and requirements.

