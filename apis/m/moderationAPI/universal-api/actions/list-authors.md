# Moderation API: List Authors

Retrieves authors from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/list-authors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/list-authors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/list-authors?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Number of authors per page |
| `pageNumber` | number | no | Page number to fetch |
| `sortBy` | string | no |  |
| `sortDirection` | string | no | Sort direction |
| `memberSinceDate` | string | no |  |
| `lastActiveDate` | string | no |  |
| `contentTypes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<object> |  |
| `pagination` | object |  |

## Native endpoint

Through the native Moderation API API, this operation is `GET /authors` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-authors.md) for the provider-specific parameters and requirements.

