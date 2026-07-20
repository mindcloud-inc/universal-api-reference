# Congress.gov: List Committee Bills

Retrieves bills for a committee from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-committee-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-committee-bills?connectionId=$CONNECTION_ID&limit=25&offset=0&chamber=house&committeeCode=hspw00" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "chamber": "house",
  "committeeCode": "hspw00"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-committee-bills?${params}`, {
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
| `chamber` | string | yes | The chamber name. Values include house, senate, or joint. Example: `house`. |
| `committeeCode` | string | yes | The committee code. For example, hspw00. Example: `hspw00`. |

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

Through the native Congress.gov API, this operation is `GET /committee/:chamber/:committeeCode/bills` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-committee-bills.md) for the provider-specific parameters and requirements.

