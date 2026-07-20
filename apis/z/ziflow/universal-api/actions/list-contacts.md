# Ziflow: List Contacts

Retrieves contacts from your Ziflow account.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "blocked": true,
          "company": "string",
          "email": "ava@example.com",
          "first_name": "Ava",
          "id": "string",
          "language": "string",
          "last_name": "Chen",
          "phone": "string",
          "proofing_defaults": {
            "comment": true,
            "decision": true,
            "manage": true,
            "notification": "string",
            "share": true,
            "view": true
          },
          "roles": [
            "string"
          ],
          "tenant": {
            "company_name": "Ava Chen",
            "subdomain": "string",
            "tenant_id": "string"
          },
          "timezone": "string",
          "type": "string",
          "verified": true
        }
      ],
      "count": 1,
      "has_more": true,
      "page": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].blocked` | boolean |  |
| `contacts[].company` | string |  |
| `contacts[].email` | string |  |
| `contacts[].first_name` | string |  |
| `contacts[].id` | string |  |
| `contacts[].language` | string |  |
| `contacts[].last_name` | string |  |
| `contacts[].phone` | string |  |
| `contacts[].proofing_defaults.comment` | boolean |  |
| `contacts[].proofing_defaults.decision` | boolean |  |
| `contacts[].proofing_defaults.manage` | boolean |  |
| `contacts[].proofing_defaults.notification` | string |  |
| `contacts[].proofing_defaults.share` | boolean |  |
| `contacts[].proofing_defaults.view` | boolean |  |
| `contacts[].roles[]` | string |  |
| `contacts[].tenant.company_name` | string |  |
| `contacts[].tenant.subdomain` | string |  |
| `contacts[].tenant.tenant_id` | string |  |
| `contacts[].timezone` | string |  |
| `contacts[].type` | string |  |
| `contacts[].verified` | boolean |  |
| `count` | number |  |
| `has_more` | boolean |  |
| `page` | number |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /contacts` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

