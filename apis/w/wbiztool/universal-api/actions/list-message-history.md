# Wbiztool: List Message History

Retrieves WhatsApp message history from Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-message-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-message-history?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-message-history?${params}`, {
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
| `startDate` | string | yes | Start date in DD-MM-YYYY format. |
| `endDate` | string | yes | End date in DD-MM-YYYY format. |
| `page` | number | no | Results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": "string",
      "id": 1,
      "messageStatus": "string",
      "msgType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string |  |
| `id` | number |  |
| `messageStatus` | string |  |
| `msgType` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /report/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-history.md) for the provider-specific parameters and requirements.

