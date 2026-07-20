# Avoma: List Calls

Retrieves calls from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-calls?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-calls?${params}`, {
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
| `fromDate` | string | yes | Retrieve calls started at or after this UTC datetime. Use ISO 8601. |
| `toDate` | string | yes | Retrieve calls started at or before this UTC datetime. Use ISO 8601. |
| `direction` | string | no | Filter calls by direction, for example inbound or outbound. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/calls/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

