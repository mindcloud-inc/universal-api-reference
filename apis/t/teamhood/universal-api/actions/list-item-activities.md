# Teamhood: List Item Activities

Retrieves Teamhood item activities for a board and time range.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-item-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-item-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-item-activities?${params}`, {
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
| `boardId` | string | no | The Teamhood board ID. |
| `endDate` | string | no | The inclusive activity window end in ISO 8601 format. |
| `startDate` | string | no | The inclusive activity window start in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "hasMore": true,
      "limit": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | Board item activity entries for the requested time window. |
| `hasMore` | boolean | Whether more activity entries are available. |
| `limit` | number | The activity page size. |
| `offset` | number | The current activity result offset. |

## Native endpoint

Through the native Teamhood API, this operation is `POST /boards/:boardId/item-activities` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-item-activities.md) for the provider-specific parameters and requirements.

