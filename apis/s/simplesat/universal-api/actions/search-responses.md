# Simplesat: Search Responses

Searches responses in Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/search-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/search-responses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/search-responses?${params}`, {
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
| `pageSize` | number | no | The number of responses to return per page |
| `page` | number | no | The page number to return |
| `startDate` | string | no |  |
| `createdStartDate` | string | no |  |
| `endDate` | string | no |  |
| `createdEndDate` | string | no |  |
| `modifiedStartDate` | string | no |  |
| `modifiedEndDate` | string | no |  |
| `operator` | string | no |  |
| `filters[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "created": "string",
      "customer": {},
      "id": 1,
      "ip_address": "string",
      "language": "string",
      "modified": "string",
      "source": "string",
      "survey": {},
      "tags": [
        "string"
      ],
      "team_members": [
        {}
      ],
      "ticket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> |  |
| `created` | string |  |
| `customer` | object |  |
| `id` | number |  |
| `ip_address` | string |  |
| `language` | string |  |
| `modified` | string |  |
| `source` | string |  |
| `survey` | object |  |
| `tags` | array<string> |  |
| `team_members` | array<object> |  |
| `ticket` | object |  |

## Native endpoint

Through the native Simplesat API, this operation is `POST /api/v1/responses/search` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-responses.md) for the provider-specific parameters and requirements.

