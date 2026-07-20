# Zoho CRM: Search Opportunity Groups

Finds Opportunity Groups in Zoho CRM by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/search-opportunity-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/search-opportunity-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/search-opportunity-groups?${params}`, {
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
| `criteria` | string | no | Use Zoho criteria syntax. To filter by Deal, use the lookup field API name from the custom module, for example `(Deal:equals:1234567890000000001)` when the field API name is `Deal`. Provide one of Criteria, Email, Phone, or Word. Example: `(Deal:equals:1234567890000000001)`. |
| `word` | string | no | Search by a free-text word. Provide one of Criteria, Email, Phone, or Word. Example: `pool`. |
| `email` | string | no | Search by an exact email address. Provide one of Criteria, Email, Phone, or Word. Example: `user@example.com`. |
| `phone` | string | no | Search by an exact phone number. Provide one of Criteria, Email, Phone, or Word. Example: `+1 555 555 5555`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated API names of fields to include in the response. Example: `Name,Deal,Total_Price,Description`. |
| `converted` | boolean | no | Whether to include converted records in the result. |
| `approved` | boolean | no | Whether to restrict the result to approved records. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho CRM API returns.

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /Opportunity_Groups/search` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-opportunity-groups.md) for the provider-specific parameters and requirements.

