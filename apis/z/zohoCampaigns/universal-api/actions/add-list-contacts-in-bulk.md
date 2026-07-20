# Zoho Campaigns: Add List Contacts in Bulk

Adds contacts to a Zoho Campaigns list in bulk.

```
POST https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-list-contacts-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-list-contacts-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listKey": "string",
  "emailIds": "alice@example.com,bob@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-list-contacts-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listKey": "string",
    "emailIds": "alice@example.com,bob@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listKey` | list<string> | yes | List key to add contacts to. |
| `emailIds` | string | yes | Up to ten email addresses, separated by commas. Accepts multiple values in one string, delimited by `,`. Example: `alice@example.com,bob@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "existingContacts": [
        "string"
      ],
      "ignoredContacts": [
        "string"
      ],
      "listkey": "string",
      "listname": "Ava Chen",
      "readdContacts": [
        "string"
      ],
      "status": "string",
      "url": "https://example.com",
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
| `existingContacts` | array<string> | Contacts already present in the list. |
| `ignoredContacts` | array<string> | Contacts ignored by Zoho. |
| `listkey` | string | Zoho list key. |
| `listname` | string | Zoho list name. |
| `readdContacts` | array<string> | Contacts re-added by Zoho. |
| `status` | string | Zoho status string. |
| `url` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /addlistsubscribersinbulk` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-list-contacts-in-bulk.md) for the provider-specific parameters and requirements.

