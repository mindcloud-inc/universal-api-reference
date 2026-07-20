# Halo Service Solutions: View Tickets

Retrieves tickets from a Halo Service Solutions ticket view.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/view-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/view-tickets?connectionId=$CONNECTION_ID&%5B%5D=%5Bobject%20Object%5D&%5B%5D.id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "[]": "[object Object]",
  "[].id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/view-tickets?${params}`, {
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
| `[]` | array<object> | yes | Array of ticket objects to view. |
| `[].id` | number | yes | Ticket ID inside the request array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_open_search_score": 1,
      "changeseq": 1,
      "id": 1,
      "lastincomingemail": "2026-05-07T12:00:00.000Z",
      "table": 1,
      "use": "string",
      "viewers": [
        {}
      ],
      "visible_child_tickets": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_open_search_score` | number |  |
| `changeseq` | number |  |
| `id` | number |  |
| `lastincomingemail` | date |  |
| `table` | number |  |
| `use` | string |  |
| `viewers` | array<object> |  |
| `visible_child_tickets` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /Tickets/View` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-tickets.md) for the provider-specific parameters and requirements.

