# Smsmobileapi: List Missed Calls

Retrieves missed calls from Smsmobileapi.

```
GET https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-missed-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smsmobileapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-missed-calls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmobileapi/latest/actions/list-missed-calls?${params}`, {
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
| `offset` | number | no | Pagination offset. The provider defaults this to 0. |
| `limit` | number | no | Maximum number of rows to return. The provider defaults to 100 and caps at 500. |
| `search` | string | no | Search by caller number or cached contact name. |
| `date_start` | date | no | Only include calls from this day onward. |
| `date_end` | date | no | Only include calls up to this day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {}
      ],
      "limit": 1,
      "offset": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of rows returned in data. |
| `data` | array<object> | Missed call rows returned by the provider. |
| `limit` | number | Pagination limit applied by the provider. |
| `offset` | number | Pagination offset applied by the provider. |
| `success` | boolean | Whether the missed-calls lookup succeeded. |

## Native endpoint

Through the native Smsmobileapi API, this operation is `GET /call/missed/list/` (base URL `https://api.smsmobileapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-missed-calls.md) for the provider-specific parameters and requirements.

