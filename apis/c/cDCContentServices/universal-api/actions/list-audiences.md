# CDC Content Services: List Audiences

Retrieves audiences from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDC Content Services `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-audiences?${params}`, {
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
| `language` | string | no | Language filter; CDC defaults to English when omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayOrdinal": 1,
      "id": 1,
      "items": [
        {}
      ],
      "language": "string",
      "mediaUsageCount": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Audience description. |
| `displayOrdinal` | number | Display order. |
| `id` | number | Audience identifier. |
| `items` | array<object> | Child audience items. |
| `language` | string | Audience language. |
| `mediaUsageCount` | number | Number of tagged media items. |
| `name` | string | Audience name. |

## Native endpoint

Through the native CDC Content Services API, this operation is `GET /v2/resources/audiences` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audiences.md) for the provider-specific parameters and requirements.

