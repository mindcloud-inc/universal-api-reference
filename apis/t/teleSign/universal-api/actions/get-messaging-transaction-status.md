# TeleSign: Get Messaging Transaction Status



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-messaging-transaction-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-messaging-transaction-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-messaging-transaction-status?${params}`, {
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
      "additional_info": {
        "mcc": "string",
        "mnc": "string"
      },
      "channel_status": [
        {}
      ],
      "currency": "string",
      "price": "string",
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string",
        "last_channel": "string",
        "updated_on": "string"
      },
      "verify": {
        "code_entered": "string",
        "code_state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional_info.mcc` | string |  |
| `additional_info.mnc` | string |  |
| `channel_status` | array<object> |  |
| `currency` | string |  |
| `price` | string |  |
| `reference_id` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.last_channel` | string |  |
| `status.updated_on` | string |  |
| `verify.code_entered` | string |  |
| `verify.code_state` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `GET /v1/omnichannel/{reference_id}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messaging-transaction-status.md) for the provider-specific parameters and requirements.

