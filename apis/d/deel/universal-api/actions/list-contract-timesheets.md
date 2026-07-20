# Deel: List Contract Timesheets

Retrieves timesheets for a contract from Deel.

```
GET https://connect.mindcloud.co/v1/universal/deel/latest/actions/list-contract-timesheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deel/latest/actions/list-contract-timesheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deel/latest/actions/list-contract-timesheets?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |

## Native endpoint

Through the native Deel API, this operation is `GET /contracts/:contract_id/timesheets` (base URL `https://api.letsdeel.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contract-timesheets.md) for the provider-specific parameters and requirements.

