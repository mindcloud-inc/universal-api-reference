# TeleSign: Get Phone Live Status



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-phone-live-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-phone-live-status?connectionId=$CONNECTION_ID&completePhoneNumber=string&ucid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "completePhoneNumber": "string",
  "ucid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-phone-live-status?${params}`, {
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
| `completePhoneNumber` | string | yes |  |
| `ucid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": {
        "name": "Ava Chen"
      },
      "errors": [
        {}
      ],
      "live": {
        "device_status": "string",
        "roaming": "string",
        "subscriber_status": "string"
      },
      "numbering": {
        "original": {
          "complete_phone_number": "string"
        }
      },
      "phone_type": {
        "description": "string"
      },
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      },
      "sub_resource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier.name` | string |  |
| `errors` | array<object> |  |
| `live.device_status` | string |  |
| `live.roaming` | string |  |
| `live.subscriber_status` | string |  |
| `numbering.original.complete_phone_number` | string |  |
| `phone_type.description` | string |  |
| `reference_id` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.updated_on` | string |  |
| `sub_resource` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `GET /v1/phoneid/live/{complete_phone_number}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-phone-live-status.md) for the provider-specific parameters and requirements.

