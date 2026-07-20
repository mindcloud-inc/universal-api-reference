# Zoho Campaigns: Add New List and Contacts

Creates a mailing list and contacts in Zoho Campaigns.

```
POST https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-new-list-and-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-new-list-and-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailIds": "alice@example.com,bob@example.com",
  "listName": "Newsletter Subscribers",
  "signupForm": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-new-list-and-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailIds": "alice@example.com,bob@example.com",
    "listName": "Newsletter Subscribers",
    "signupForm": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailIds` | string | yes | Up to ten email addresses to add to the new list. Accepts multiple values in one string, delimited by `,`. Example: `alice@example.com,bob@example.com`. |
| `listName` | string | yes | Name of the new mailing list. Example: `Newsletter Subscribers`. |
| `signupForm` | string | yes | Signup form visibility for the new list. One of: `0`, `1`. |
| `listDescription` | string | no | Description for the new mailing list. Example: `Contacts imported from signup form`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "listKey": "string",
      "listName": "Ava Chen",
      "message": "string",
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
| `listKey` | string | Created Zoho mailing list key. |
| `listName` | string | Created Zoho mailing list name. |
| `message` | string | Provider message for the list creation attempt. |
| `uri` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /addlistandcontacts` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-list-and-contacts.md) for the provider-specific parameters and requirements.

