# Salesforge: Get Contact

Retrieves a contact from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-contact?connectionId=$CONNECTION_ID&workspaceId=wks_lxxtq91neaixc8yaiqp7w&contactId=lead_n539nxku3oq5k3w1cc5py" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w",
  "contactId": "lead_n539nxku3oq5k3w1cc5py"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |
| `contactId` | string | yes | Example: `lead_n539nxku3oq5k3w1cc5py`. |

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

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/contacts/:contactID` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

