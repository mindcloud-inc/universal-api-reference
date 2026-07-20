# Nutshell: List Notes

Retrieves notes from Nutshell.

```
GET https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutshell `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-notes?${params}`, {
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
      "body": "string",
      "bodyMarkup": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "deletedTime": {},
      "href": "string",
      "htmlUrl": "https://example.com",
      "htmlUrlPath": "https://example.com",
      "id": "string",
      "isEditable": true,
      "links": {
        "parent": "https://example.com"
      },
      "parentType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `bodyMarkup` | string |  |
| `createdTime` | date |  |
| `deletedTime` | object |  |
| `href` | string |  |
| `htmlUrl` | string |  |
| `htmlUrlPath` | string |  |
| `id` | string |  |
| `isEditable` | boolean |  |
| `links.parent` | string |  |
| `parentType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Nutshell API, this operation is `GET /notes` (base URL `https://app.nutshell.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

