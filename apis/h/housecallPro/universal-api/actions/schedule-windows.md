# Housecall Pro: Schedule Windows



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/schedule-windows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/schedule-windows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/schedule-windows?${params}`, {
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
      "availabilityBufferInDays": 1,
      "dailyAvailabilities": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityBufferInDays` | number |  |
| `dailyAvailabilities` | object |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /company/schedule_availability` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-windows.md) for the provider-specific parameters and requirements.

