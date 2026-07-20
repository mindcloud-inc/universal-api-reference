# Mobile Text Alerts: Get Subscriber

Finds a subscriber in Mobile Text Alerts by ID, number, or email.

```
GET https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mobile Text Alerts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&idOrNumberOrEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrNumberOrEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/get-subscriber?${params}`, {
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
| `idOrNumberOrEmail` | string | yes | Subscriber ID, phone number, or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Subscriber returned by Mobile Text Alerts. |
| `message` | string | Optional API response message. |

## Native endpoint

Through the native Mobile Text Alerts API, this operation is `GET /subscribers/:idOrNumberOrEmail` (base URL `https://api.mobile-text-alerts.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

