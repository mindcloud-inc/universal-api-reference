# PagePixels: List All Change Notifications



```
GET https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-all-change-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-all-change-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-all-change-notifications?${params}`, {
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
| `page` | number | no | The result page to retrieve. |
| `limit` | number | no | The number of records to retrieve. |
| `after` | number | no | Only include records created after this unix timestamp. |
| `before` | number | no | Only include records created before this unix timestamp. |
| `order` | string | no | Sort order, either ASC or DESC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "id": "string",
      "previousValue": "string",
      "retrievedValue": "string",
      "screenshotConfigurationId": "string",
      "sentAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | The change notification rule configuration returned by PagePixels. |
| `id` | string | The unique identifier for the change notification record. |
| `previousValue` | string | The previously captured selector value before the detected change. |
| `retrievedValue` | string | The newly captured selector value that triggered the notification. |
| `screenshotConfigurationId` | string | The screenshot configuration ID that produced the notification. |
| `sentAt` | string | The timestamp when PagePixels sent the notification webhook. |

## Native endpoint

Through the native PagePixels API, this operation is `GET /change_notifications` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-change-notifications.md) for the provider-specific parameters and requirements.

