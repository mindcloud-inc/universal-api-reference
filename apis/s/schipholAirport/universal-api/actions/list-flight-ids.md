# Schiphol Airport: List Flight IDs

Retrieves flight IDs from Schiphol Airport by datetime range.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-flight-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-flight-ids?connectionId=$CONNECTION_ID&fromDateTime=string&toDateTime=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDateTime": "string",
  "toDateTime": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-flight-ids?${params}`, {
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
| `fromDateTime` | string | yes | Start of the scheduleDateTime range, formatted yyyy-MM-ddTHH:mm:ss. |
| `toDateTime` | string | yes | End of the scheduleDateTime range, formatted yyyy-MM-ddTHH:mm:ss. Maximum range is three days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Schiphol flight ID |

## Native endpoint

Through the native Schiphol Airport API, this operation is `GET /flights/ids` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flight-ids.md) for the provider-specific parameters and requirements.

