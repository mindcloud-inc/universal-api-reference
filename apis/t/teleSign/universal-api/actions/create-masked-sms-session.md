# TeleSign: Create Masked SMS Session



```
POST https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/create-masked-sms-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/create-masked-sms-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/create-masked-sms-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "external_id": "string",
      "reference_id": "string",
      "session_data": {
        "phone_number_1": {
          "masked_id": "string"
        },
        "phone_number_2": {
          "masked_id": "string"
        },
        "resource": "string",
        "session_end_on": "string",
        "validity": "string"
      },
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_id` | string |  |
| `reference_id` | string |  |
| `session_data.phone_number_1.masked_id` | string |  |
| `session_data.phone_number_2.masked_id` | string |  |
| `session_data.resource` | string |  |
| `session_data.session_end_on` | string |  |
| `session_data.validity` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.updated_on` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `POST /v1/anonymous/session/sms` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-masked-sms-session.md) for the provider-specific parameters and requirements.

