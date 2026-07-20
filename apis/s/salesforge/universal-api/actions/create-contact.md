# Salesforge: Create Contact

Creates a contact in Salesforge.

```
POST https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "wks_989gtkhm1ir6z8hdv3gjn",
  "firstName": "Avery"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "wks_989gtkhm1ir6z8hdv3gjn",
    "firstName": "Avery"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `firstName` | string | yes | Example: `Avery`. |
| `lastName` | string | no | Example: `Stone`. |
| `email` | string | no | Example: `avery.stage3.salesforge@example.com`. |
| `company` | string | no | Example: `MindCloud`. |
| `position` | string | no | Example: `Revenue Operations`. |
| `linkedinUrl` | string | no | Example: `https://www.linkedin.com/in/avery-stone`. |
| `tagIds[]` | array<string> | no | Example: `tag_123`. |
| `tags[]` | array<string> | no | Example: `stage3`. |
| `customVars` | object | no | Map of custom variable keys to string values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "customVars": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `customVars` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `linkedinUrl` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Salesforge API, this operation is `POST /public/v2/workspaces/:workspaceID/contacts` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

