# GIRITON: List Users Employed Between Dates

Retrieves users employed during a selected GIRITON date range.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-users-employed-between-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-users-employed-between-dates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-users-employed-between-dates?${params}`, {
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
| `employedFrom` | string | no | Start of the employment interval. |
| `employedTo` | string | no | End of the employment interval. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "entries": [
        {}
      ],
      "newestTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of returned entries. |
| `entries` | array<object> | Employee entries. |
| `newestTimestamp` | date | Newest entry timestamp. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /hr/usersEmployedBetween` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users-employed-between-dates.md) for the provider-specific parameters and requirements.

