# Envoice: Search Work Types

Finds work types in Envoice by query.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/search-work-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/search-work-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/search-work-types?${params}`, {
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
| `order` | string | no | Sort direction for work type search results. |
| `orderBy` | string | no | Field to order work type search results by. |
| `page` | number | no | Result page number. |
| `pageSize` | number | no | Number of results per page. |
| `query` | string | no | Search text for matching work types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Count": 1,
      "ErrorMessages": [
        "string"
      ],
      "IsFaulted": true,
      "Result": [
        {}
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Count` | number | Number of work types in the current response. |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `IsFaulted` | boolean | Whether the request failed. |
| `Result` | array<object> | Work types returned by Envoice. |
| `TotalCount` | number | Total work types matching the search. |

## Native endpoint

Through the native Envoice API, this operation is `GET worktype/search` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-work-types.md) for the provider-specific parameters and requirements.

