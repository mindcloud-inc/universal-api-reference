# ChurchStamp: Send Mail

Sends campaign mail to a recipient in ChurchStamp.

```
POST https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/send-mail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChurchStamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/send-mail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "1731535111267x707091876624990200",
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/send-mail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "1731535111267x707091876624990200",
    "firstName": "John",
    "lastName": "Doe",
    "email": "john@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Unique identifier for the campaign used to send mail. Example: `1731535111267x707091876624990200`. |
| `firstName` | string | yes | Recipient first name. Example: `John`. |
| `lastName` | string | yes | Recipient last name. Example: `Doe`. |
| `email` | string | yes | Recipient email address. Example: `john@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_id": "string",
      "Created By": "string",
      "Created Date": 1,
      "email": "ava@example.com",
      "mail_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | string |  |
| `Created By` | string |  |
| `Created Date` | number |  |
| `email` | string |  |
| `mail_id` | string |  |

## Native endpoint

Through the native ChurchStamp API, this operation is `POST /campaign-sendmail` (base URL `https://v2.churchstamp.com/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-mail.md) for the provider-specific parameters and requirements.

