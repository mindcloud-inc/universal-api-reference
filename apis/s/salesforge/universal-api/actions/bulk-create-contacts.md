# Salesforge: Bulk Create Contacts

Creates contacts in bulk in Salesforge.

```
POST https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/bulk-create-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/bulk-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
  "contacts[]": [
    {}
  ],
  "contacts[].firstName": "Avery"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/bulk-create-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
    "contacts[]": [{}],
    "contacts[].firstName": "Avery"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |
| `contacts[]` | array<object> | yes |  |
| `contacts[].firstName` | string | yes | Example: `Avery`. |
| `contacts[].lastName` | string | no | Example: `Stone`. |
| `contacts[].email` | string | no | Example: `avery.bulk@example.com`. |
| `contacts[].company` | string | no | Example: `MindCloud`. |
| `contacts[].position` | string | no | Example: `Revenue Operations`. |
| `contacts[].linkedinUrl` | string | no | Example: `https://www.linkedin.com/in/avery-stone`. |
| `contacts[].tagIds[]` | array<string> | no | Example: `tag_123`. |
| `contacts[].tags[]` | array<string> | no | Example: `stage3`. |
| `contacts[].customVars` | object | no | Map of custom variable keys to string values for each contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> |  |

## Native endpoint

Through the native Salesforge API, this operation is `POST /public/v2/workspaces/:workspaceID/contacts/bulk` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-contacts.md) for the provider-specific parameters and requirements.

