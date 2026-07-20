# SendMails: Update Campaign

Updates an existing campaign in SendMails.

```
PUT https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | Campaign UID from SendMails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Updated campaign attributes. |
| `message` | string | Provider result message. |
| `status` | number | Provider success indicator. |

## Native endpoint

Through the native SendMails API, this operation is `PATCH /campaigns/:uid` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

