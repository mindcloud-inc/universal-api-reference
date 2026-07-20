# Platerecognizer: Get VIN Statistics

Retrieves your Plate Recognizer VIN ID usage statistics.

```
GET https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/get-vin-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platerecognizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/get-vin-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/get-vin-statistics?${params}`, {
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
      "totalCalls": 1,
      "usage": {
        "calls": 1,
        "month": 1,
        "resetsOn": "2026-05-07T12:00:00.000Z",
        "year": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalCalls` | number |  |
| `usage.calls` | number |  |
| `usage.month` | number |  |
| `usage.resetsOn` | date |  |
| `usage.year` | number |  |

## Native endpoint

Through the native Platerecognizer API, this operation is `GET /vin/statistics/` (base URL `https://api.platerecognizer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vin-statistics.md) for the provider-specific parameters and requirements.

