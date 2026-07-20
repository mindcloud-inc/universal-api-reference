# Congress.gov: List Summaries By Congress

Retrieves bill summaries from a specific Congress in Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-summaries-by-congress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-summaries-by-congress?connectionId=$CONNECTION_ID&limit=25&offset=0&congress=118" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "congress": "118"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-summaries-by-congress?${params}`, {
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
| `congress` | number | yes | The congress number. For example, 118. Example: `118`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "request": {},
      "summaries": [
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
| `pagination` | object |  |
| `request` | object |  |
| `summaries` | array<object> |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /summaries/:congress` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-summaries-by-congress.md) for the provider-specific parameters and requirements.

