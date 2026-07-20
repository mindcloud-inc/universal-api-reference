# TaxBandits: Test Connection

Retrieves TaxBandits API connection status and version details.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/test-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/test-connection?${params}`, {
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
      "APIVersion": "string",
      "Errors": [
        {}
      ],
      "JWTExpiry": "string",
      "StatusCode": 1,
      "StatusMessage": "string",
      "StatusName": "Ava Chen",
      "TimeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `APIVersion` | string |  |
| `Errors` | array<object> |  |
| `JWTExpiry` | string |  |
| `StatusCode` | number |  |
| `StatusMessage` | string |  |
| `StatusName` | string |  |
| `TimeZone` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET Utility/Ping` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-connection.md) for the provider-specific parameters and requirements.

