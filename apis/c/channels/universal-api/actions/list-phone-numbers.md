# Channels: List Phone Numbers

Retrieves phone numbers from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-phone-numbers?${params}`, {
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
      "": [
        {
          "availableForSms": true,
          "eea": true,
          "id": 1,
          "initial": true,
          "isoCountry": "string",
          "label": "string",
          "msisdn": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].availableForSms` | boolean |  |
| `[].eea` | boolean |  |
| `[].id` | number |  |
| `[].initial` | boolean |  |
| `[].isoCountry` | string |  |
| `[].label` | string |  |
| `[].msisdn` | string |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/msisdns` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phone-numbers.md) for the provider-specific parameters and requirements.

