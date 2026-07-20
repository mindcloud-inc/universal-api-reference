# Freshdesk: Create Company

Creates a new company in Freshdesk.

```
POST https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields` | object | no | Key-value pairs for custom company fields |
| `description` | string | no | Description of the company |
| `domains[]` | array<string> | no | Domains associated with the company |
| `name` | string | yes | Name of the company |
| `note` | string | no | Specific note about the company |
| `healthScore` | string | no | Relationship strength with the company |
| `accountTier` | string | no | Business value classification tier |
| `renewalDate` | date | no | Contract or relationship renewal date |
| `industry` | string | no | Industry the company serves in |
| `lookupParameter` | string | no | Lookup field value for custom object linkage |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTier": "string",
      "createdAt": "string",
      "description": "string",
      "domains": [
        "string"
      ],
      "id": 1,
      "industry": "string",
      "name": "Ava Chen",
      "note": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTier` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `domains` | array<string> |  |
| `id` | number |  |
| `industry` | string |  |
| `name` | string |  |
| `note` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `POST /companies` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

