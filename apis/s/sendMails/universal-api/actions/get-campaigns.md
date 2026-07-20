# SendMails: Get Campaigns

Retrieves a list of campaigns from SendMails.

```
GET https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-campaigns?${params}`, {
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
      "deliveryAt": "string",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "name": "Ava Chen",
      "replyTo": "string",
      "sentLabel": "string",
      "sentPercent": "string",
      "status": "string",
      "subject": "string",
      "subscribers": "string",
      "type": "string",
      "uid": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `deliveryAt` | string | Scheduled delivery timestamp if present. |
| `fromEmail` | string | From email address. |
| `fromName` | string | From display name. |
| `name` | string | Campaign name. |
| `replyTo` | string | Reply-to email address. |
| `sentLabel` | string | Provider sent label. |
| `sentPercent` | string | Provider sent percentage field. |
| `status` | string | Campaign status. |
| `subject` | string | Campaign subject. |
| `subscribers` | string | Provider subscriber summary field. |
| `type` | string | Campaign type. |
| `uid` | string | Campaign UID. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native SendMails API, this operation is `GET /campaigns` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaigns.md) for the provider-specific parameters and requirements.

