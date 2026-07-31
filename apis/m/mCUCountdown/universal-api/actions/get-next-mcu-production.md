# MCU Countdown: Get Next MCU Production



```
GET https://connect.mindcloud.co/v1/universal/mCUCountdown/latest/actions/get-next-mcu-production
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MCU Countdown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mCUCountdown/latest/actions/get-next-mcu-production?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mCUCountdown/latest/actions/get-next-mcu-production?${params}`, {
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
      "days_until": 1,
      "following_production": {
        "days_until": 1,
        "id": 1,
        "overview": "string",
        "poster_url": "https://example.com",
        "release_date": "string",
        "title": "string",
        "type": "string"
      },
      "id": 1,
      "overview": "string",
      "poster_url": "https://example.com",
      "release_date": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `days_until` | number |  |
| `following_production` | object |  |
| `following_production.days_until` | number |  |
| `following_production.id` | number |  |
| `following_production.overview` | string |  |
| `following_production.poster_url` | string |  |
| `following_production.release_date` | string |  |
| `following_production.title` | string |  |
| `following_production.type` | string |  |
| `id` | number |  |
| `overview` | string |  |
| `poster_url` | string |  |
| `release_date` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native MCU Countdown API, this operation is `GET /api` (base URL `https://whenisthenextmcufilm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-next-mcu-production.md) for the provider-specific parameters and requirements.

