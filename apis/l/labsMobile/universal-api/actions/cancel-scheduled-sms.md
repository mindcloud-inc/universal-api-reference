# LabsMobile: Cancel Scheduled SMS

Cancels a scheduled SMS message in LabsMobile.

```
DELETE https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/cancel-scheduled-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LabsMobile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/cancel-scheduled-sms?connectionId=$CONNECTION_ID&subid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/cancel-scheduled-sms?${params}`, {
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
| `subid` | string | yes | Identifier for the scheduled send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |

## Native endpoint

Through the native LabsMobile API, this operation is `POST /json/scheduled` (base URL `https://api.labsmobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-scheduled-sms.md) for the provider-specific parameters and requirements.

