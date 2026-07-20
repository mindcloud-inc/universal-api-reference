# SuperSend: Bulk Import Contacts

Creates multiple contacts in SuperSend.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/bulk-import-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/bulk-import-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ],
  "teamId": "string",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/bulk-import-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}],
    "teamId": "string",
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes |  |
| `contacts[].email` | string | no |  |
| `contacts[].linkedinUrl` | string | no |  |
| `contacts[].twitter` | string | no |  |
| `contacts[].firstName` | string | no |  |
| `contacts[].lastName` | string | no |  |
| `contacts[].companyName` | string | no |  |
| `contacts[].title` | string | no |  |
| `contacts[].phone` | string | no |  |
| `contacts[].city` | string | no |  |
| `contacts[].state` | string | no |  |
| `contacts[].country` | string | no |  |
| `contacts[].industry` | string | no |  |
| `contacts[].companyUrl` | string | no |  |
| `contacts[].note` | string | no |  |
| `contacts[].oneLiner` | string | no |  |
| `contacts[].custom` | object | no |  |
| `teamId` | string | yes |  |
| `campaignId` | string | yes |  |
| `validateEmails` | boolean | no | When true, runs email verification on imported contacts (consumes credits). Default false to avoid surprise billing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_count": 1,
      "message": "string",
      "status": "string",
      "upload_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_count` | number |  |
| `message` | string |  |
| `status` | string |  |
| `upload_id` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /contacts/bulk` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-import-contacts.md) for the provider-specific parameters and requirements.

