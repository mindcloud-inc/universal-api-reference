# SendMails: Run Campaign

Runs a campaign in SendMails.

```
PUT https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/run-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/run-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/run-campaign', {
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
      "campaign": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object | Launched campaign summary. |
| `message` | string | Provider result message. |
| `status` | string | Provider result status. |

## Native endpoint

Through the native SendMails API, this operation is `POST /campaigns/:uid/run` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-campaign.md) for the provider-specific parameters and requirements.

