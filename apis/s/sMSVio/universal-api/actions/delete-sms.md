# SMSVio: Delete SMS



```
DELETE https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/delete-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSVio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/delete-sms?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/delete-sms?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": {},
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | object |  |
| `status` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native SMSVio API, this operation is `POST /services/send/` (base URL `https://gate.smsvio.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sms.md) for the provider-specific parameters and requirements.

