# TouchBasePro: Get Email Statistics

Retrieves email statistics details from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-email-statistics?${params}`, {
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
      "bounces": 1,
      "clicked": 1,
      "delivered": 1,
      "opened": 1,
      "query": {
        "from": "string",
        "group": "string",
        "smartEmailId": "ava@example.com",
        "timeZone": "string",
        "to": "string"
      },
      "sent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounces` | number |  |
| `clicked` | number |  |
| `delivered` | number |  |
| `opened` | number |  |
| `query.from` | string |  |
| `query.group` | string |  |
| `query.smartEmailId` | string |  |
| `query.timeZone` | string |  |
| `query.to` | string |  |
| `sent` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/transactional/statistics` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-statistics.md) for the provider-specific parameters and requirements.

