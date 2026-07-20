# Moaform: List Forms

Retrieves forms from your Moaform account.

```
GET https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moaform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-forms?${params}`, {
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
| `search` | string | no | Search forms by title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "collection": {
            "endAt": "2026-05-07T12:00:00.000Z",
            "responsesCount": 1,
            "startAt": "2026-05-07T12:00:00.000Z"
          },
          "createdAt": "2026-05-07T12:00:00.000Z",
          "groups": [
            "string"
          ],
          "id": "string",
          "lastResponsedAt": "2026-05-07T12:00:00.000Z",
          "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
          "links": {
            "answerUrl": "https://example.com",
            "reportUrl": "https://example.com",
            "self": "https://example.com"
          },
          "longId": "string",
          "name": "Ava Chen",
          "owned": true,
          "status": "string"
        }
      ],
      "pageCount": 1,
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].collection` | object |  |
| `items[].collection.endAt` | date |  |
| `items[].collection.responsesCount` | number |  |
| `items[].collection.startAt` | date |  |
| `items[].createdAt` | date |  |
| `items[].groups` | array<string> |  |
| `items[].id` | string |  |
| `items[].lastResponsedAt` | date |  |
| `items[].lastUpdatedAt` | date |  |
| `items[].links` | object |  |
| `items[].links.answerUrl` | string |  |
| `items[].links.reportUrl` | string |  |
| `items[].links.self` | string |  |
| `items[].longId` | string |  |
| `items[].name` | string |  |
| `items[].owned` | boolean |  |
| `items[].status` | string |  |
| `pageCount` | number |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Moaform API, this operation is `GET /forms` (base URL `https://api.moaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

