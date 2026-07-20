# DitLead: Update Mailbox



```
PUT https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/update-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/update-mailbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/update-mailbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignSetting.sendingLimit` | number | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `mailboxId` | string | yes | Public ID of the mailbox. |
| `warmingSetting.increasePerDay` | number | no |  |
| `warmingSetting.maximumSendPerDay` | number | no |  |
| `warmingSetting.randomizeMax` | boolean | no |  |
| `warmingSetting.replyRate` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `PUT /v1/mailbox/{mailboxId}` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mailbox.md) for the provider-specific parameters and requirements.

