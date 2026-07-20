# Zoho Campaigns: Move Contact to Do Not Mail

Moves a contact to Zoho Campaigns do-not-mail.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/move-contact-to-do-not-mail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/move-contact-to-do-not-mail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactInfo": "{Contact Email:person@example.com}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/move-contact-to-do-not-mail', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactInfo": "{Contact Email:person@example.com}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactInfo` | string | yes | Contact payload in Zoho's documented string format. Example: `{Contact Email:person@example.com}`. |

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
| `message` | string | Provider message for the do-not-mail update. |
| `status` | string | Zoho status string. |
| `uri` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /json/contactdonotmail` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-contact-to-do-not-mail.md) for the provider-specific parameters and requirements.

