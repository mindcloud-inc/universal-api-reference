# HelloLeads: List Leads



```
GET https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelloLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-leads?${params}`, {
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
| `order` | string | no | Optional HelloLeads sort order string, for example desc as shown in the provider docs. |
| `createdDate` | string | no | Optional HelloLeads createdDate filter in provider format YYYY-MM-DD. This stays a string because HelloLeads expects the literal date string, not an ISO timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_line1": "string",
      "address_line2": "string",
      "alternatePhone": "string",
      "category": "string",
      "city": "string",
      "company": "string",
      "country": "string",
      "created": "string",
      "dealSize": "string",
      "designation": "string",
      "email": "ava@example.com",
      "fax": "string",
      "first_name": "Ava",
      "id": "string",
      "interests": "string",
      "last_name": "Chen",
      "list_name": "Ava Chen",
      "mobile": "string",
      "modified": "string",
      "notes": "string",
      "phone": "string",
      "postal_code": "string",
      "potential": "string",
      "stage": "string",
      "state": "string",
      "tags": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_line1` | string | First address line. |
| `address_line2` | string | Second address line. |
| `alternatePhone` | string | Alternate phone number returned by HelloLeads. |
| `category` | string | Lead category. |
| `city` | string | Lead city. |
| `company` | string | Company or organization name. |
| `country` | string | Lead country. |
| `created` | string | Provider timestamp when the lead was created. |
| `dealSize` | string | Deal size returned by HelloLeads. |
| `designation` | string | Lead designation or job title. |
| `email` | string | Lead email address. |
| `fax` | string | Lead fax number. |
| `first_name` | string | Lead first name. |
| `id` | string | HelloLeads lead identifier. |
| `interests` | string | Lead interests. |
| `last_name` | string | Lead last name. |
| `list_name` | string | HelloLeads list name. |
| `mobile` | string | Lead mobile number. |
| `modified` | string | Provider timestamp when the lead was last modified. |
| `notes` | string | Lead notes. |
| `phone` | string | Lead phone number. |
| `postal_code` | string | Lead postal or ZIP code. |
| `potential` | string | Lead potential returned by HelloLeads. |
| `stage` | string | Lead stage returned by HelloLeads. |
| `state` | string | Lead state or region. |
| `tags` | string | Lead tags. |
| `website` | string | Lead website URL. |

## Native endpoint

Through the native HelloLeads API, this operation is `GET leadsOrderBy` (base URL `https://app.helloleads.io/index.php/private/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

