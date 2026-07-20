# TelTel: Get Inbound SMS Report

Retrieves an inbound SMS report from TelTel.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-inbound-sms-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-inbound-sms-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-inbound-sms-report?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "id": "string",
      "message": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `from` | string |  |
| `id` | string |  |
| `message` | string |  |
| `to` | string |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /sms/inbox/reports/{id}` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbound-sms-report.md) for the provider-specific parameters and requirements.

