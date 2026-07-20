# Yay.com: List Missed Call Notifications

Retrieves missed call notifications from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-missed-call-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-missed-call-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-missed-call-notifications?${params}`, {
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
      "emailAddress": "ava@example.com",
      "includeVoicemailAnswered": true,
      "uuid": "string",
      "voipNumberUuid": "string",
      "voipUserUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string |  |
| `includeVoicemailAnswered` | boolean |  |
| `uuid` | string |  |
| `voipNumberUuid` | string |  |
| `voipUserUuid` | string |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/missed-call` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-missed-call-notifications.md) for the provider-specific parameters and requirements.

