# Zoho Campaigns: Unsubscribe Contact from List

Unsubscribes a contact from a Zoho Campaigns list.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/unsubscribe-contact-from-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/unsubscribe-contact-from-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listKey": "string",
  "contactInfo": "{First Name:Jane,Last Name:Doe,Contact Email:jane@example.com}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/unsubscribe-contact-from-list', {
  method: 'PUT',
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
| `listKey` | list<string> | yes | List key to unsubscribe the contact from. |
| `contactInfo` | string | yes | Contact payload in Zoho's documented JSON-style string format. Example: `{First Name:Jane,Last Name:Doe,Contact Email:jane@example.com}`. |

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
| `message` | string | Provider message for the unsubscribe attempt. |
| `status` | string | Zoho status string. |
| `uri` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /json/listunsubscribe` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-contact-from-list.md) for the provider-specific parameters and requirements.

