# HigherGov: List People

Retrieves people from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-people?${params}`, {
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
| `contactEmail` | string | no | Email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agency": {},
      "contact_email": "ava@example.com",
      "contact_first_name": "Ava",
      "contact_last_name": "Chen",
      "contact_name": "Ava Chen",
      "contact_phone": "string",
      "contact_title": "string",
      "contact_type": "string",
      "last_seen": "string",
      "path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agency` | object |  |
| `contact_email` | string |  |
| `contact_first_name` | string |  |
| `contact_last_name` | string |  |
| `contact_name` | string |  |
| `contact_phone` | string |  |
| `contact_title` | string |  |
| `contact_type` | string |  |
| `last_seen` | string |  |
| `path` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/people/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

