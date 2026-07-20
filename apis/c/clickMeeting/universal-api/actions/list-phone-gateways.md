# ClickMeeting: List Phone Gateways

Retrieves available phone gateways from ClickMeeting.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-phone-gateways
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-phone-gateways?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/list-phone-gateways?${params}`, {
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
      "code": "string",
      "geo": {
        "lat": 1,
        "long": 1
      },
      "location": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Country code. |
| `geo.lat` | number | Gateway latitude. |
| `geo.long` | number | Gateway longitude. |
| `location` | string | Gateway location. |
| `value` | string | Dial-in phone number. |

## Native endpoint

Through the native ClickMeeting API, this operation is `GET phone_gateways` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phone-gateways.md) for the provider-specific parameters and requirements.

