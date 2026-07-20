# Tidio: List Operators [Plus plan]

Retrieves operators from the Tidio workspace.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-operators-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-operators-plus-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-operators-plus-plan?${params}`, {
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
      "meta": {
        "cursor": "string",
        "limit": 1
      },
      "operators": [
        {
          "active": true,
          "email": "ava@example.com",
          "id": "string",
          "lastSeen": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "picture": "string",
          "role": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `meta.cursor` | string | Value to fetch the next page. Null means the page is the last one. |
| `meta.limit` | number | How many items were displayed on list |
| `operators` | array<object> |  |
| `operators[]` | object |  |
| `operators[].active` | boolean | Indicates if the operator is active |
| `operators[].email` | string | Email address of the operator |
| `operators[].id` | string | ID of the operator |
| `operators[].lastSeen` | date | Last seen operator date |
| `operators[].name` | string | Name of the operator |
| `operators[].picture` | string | URL to picture of the operator |
| `operators[].role` | string | Role of the operator |

## Native endpoint

Through the native Tidio API, this operation is `GET /operators` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-operators-plus-plan.md) for the provider-specific parameters and requirements.

