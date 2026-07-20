# TouchBasePro: Get Message Timeline

Retrieves message timeline details from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-message-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-message-timeline?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-message-timeline?${params}`, {
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
      "canBeResent": true,
      "from": "string",
      "group": "string",
      "messageId": "string",
      "recipient": "string",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "smartEmailId": 1,
      "status": "string",
      "subject": "string",
      "totalClicks": 1,
      "totalOpens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canBeResent` | boolean |  |
| `from` | string |  |
| `group` | string |  |
| `messageId` | string |  |
| `recipient` | string |  |
| `sentAt` | date |  |
| `smartEmailId` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `totalClicks` | number |  |
| `totalOpens` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/transactional/messages` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-timeline.md) for the provider-specific parameters and requirements.

