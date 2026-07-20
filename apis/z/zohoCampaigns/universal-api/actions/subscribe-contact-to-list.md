# Zoho Campaigns: Subscribe Contact to List

Subscribes a contact to a Zoho Campaigns list.

```
POST https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/subscribe-contact-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/subscribe-contact-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listKey": "string",
  "contactInfo": "{First Name:Jane,Last Name:Doe,Contact Email:jane@example.com}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/subscribe-contact-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listKey": "string",
    "contactInfo": "{First Name:Jane,Last Name:Doe,Contact Email:jane@example.com}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listKey` | list<string> | yes | List key to subscribe the contact to. |
| `contactInfo` | string | yes | Contact payload in Zoho's documented JSON-style string format. Example: `{First Name:Jane,Last Name:Doe,Contact Email:jane@example.com}`. |
| `source` | string | no | Optional source label recorded for the contact. Example: `Signup form`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topicId` | list<string> | no | Topic ID required on accounts that use Zoho's updated topic management. Example: `1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string",
      "status": "string",
      "uri": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Zoho result code. |
| `message` | string | Provider message for the subscribe attempt. |
| `status` | string | Zoho status string. |
| `uri` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /json/listsubscribe` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-contact-to-list.md) for the provider-specific parameters and requirements.

