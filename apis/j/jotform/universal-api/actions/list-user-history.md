# Jotform: List User History

Retrieves user history entries from Jotform.

```
GET https://connect.mindcloud.co/v1/universal/jotform/latest/actions/list-user-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/list-user-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/list-user-history?${params}`, {
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
| `action` | string | no | Filter history by action type. |
| `date` | string | no | Filter history by a specific date. |
| `endDate` | string | no | History end date. |
| `sortBy` | string | no | Sort history by field. |
| `startDate` | string | no | History start date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ip": "string",
      "timestamp": 1,
      "type": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ip` | string |  |
| `timestamp` | number |  |
| `type` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `GET /user/history` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-history.md) for the provider-specific parameters and requirements.

