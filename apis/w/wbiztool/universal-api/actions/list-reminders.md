# Wbiztool: List Reminders

Retrieves active reminders from Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-reminders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-reminders?${params}`, {
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
| `page` | number | no | Results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "cronExpression": "string",
      "fileName": "Ava Chen",
      "id": 1,
      "imgUrl": "https://example.com",
      "isActive": true,
      "messageTemplate": "string",
      "msgType": 1,
      "msgTypeDisplay": "string",
      "name": "Ava Chen",
      "nextRun": "2026-05-07T12:00:00.000Z",
      "toNumber": "string",
      "whatsappClientId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `cronExpression` | string |  |
| `fileName` | string |  |
| `id` | number |  |
| `imgUrl` | string |  |
| `isActive` | boolean |  |
| `messageTemplate` | string |  |
| `msgType` | number |  |
| `msgTypeDisplay` | string |  |
| `name` | string |  |
| `nextRun` | date |  |
| `toNumber` | string |  |
| `whatsappClientId` | number |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /reminder/list/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reminders.md) for the provider-specific parameters and requirements.

