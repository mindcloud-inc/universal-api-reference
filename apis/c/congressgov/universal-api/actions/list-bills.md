# Congress.gov: List Bills

Retrieves bills from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-bills?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-bills?${params}`, {
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
| `fromDateTime` | date | no | Starting timestamp to filter by update date. Use YYYY-MM-DDT00:00:00Z. Example: `2026-01-01T00:00:00Z`. |
| `toDateTime` | date | no | Ending timestamp to filter by update date. Use YYYY-MM-DDT00:00:00Z. Example: `2026-04-01T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bills": [
        {}
      ],
      "pagination": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bills` | array<object> |  |
| `pagination` | object |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /bill` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bills.md) for the provider-specific parameters and requirements.

