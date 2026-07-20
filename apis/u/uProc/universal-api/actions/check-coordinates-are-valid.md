# UProc: Check Coordinates Are Valid



```
GET https://connect.mindcloud.co/v1/universal/uProc/latest/actions/check-coordinates-are-valid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UProc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uProc/latest/actions/check-coordinates-are-valid?connectionId=$CONNECTION_ID&coordinates=41.2522%2C-12.30" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "coordinates": "41.2522,-12.30"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uProc/latest/actions/check-coordinates-are-valid?${params}`, {
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
| `coordinates` | string | yes | Latitude and longitude pair to validate. Default: `41.2522,-12.30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "criteria": "string",
      "error": true,
      "message": {},
      "normalized": true,
      "params": {},
      "price": 1,
      "processor": "string",
      "realPrice": 1,
      "result": true,
      "time": 1,
      "totalRows": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Remaining account balance when returned. |
| `criteria` | string | Applied matching criteria when returned. |
| `error` | boolean | Provider error flag when returned. |
| `message` | object | Processor response payload. |
| `normalized` | boolean | Normalization flag when returned. |
| `params` | object | Normalized processor input parameters. |
| `price` | number | Request price when returned. |
| `processor` | string | Executed uProc processor key. |
| `realPrice` | number | Effective request price when returned. |
| `result` | boolean | Processor result flag. |
| `time` | number | Execution time when returned. |
| `totalRows` | number | Total processed rows when returned. |

## Native endpoint

Through the native UProc API, this operation is `POST /process` (base URL `https://api.uproc.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-coordinates-are-valid.md) for the provider-specific parameters and requirements.

