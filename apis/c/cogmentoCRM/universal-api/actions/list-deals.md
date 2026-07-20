# Cogmento CRM: List Deals



```
GET https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-deals?${params}`, {
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
      "access": {
        "private": true
      },
      "accountId": "string",
      "acl": [
        {}
      ],
      "amount": 1,
      "assignedTo": [
        {}
      ],
      "auxId": "string",
      "auxSource": "string",
      "auxSourceName": "Ava Chen",
      "closed": true,
      "closeDate": "string",
      "company": {},
      "contacts": [
        {}
      ],
      "createdAt": "string",
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "notificationOptIn": true
      },
      "dealProducts": [
        {}
      ],
      "description": "string",
      "flags": {
        "callAssigned": true,
        "caseAssigned": true,
        "emailReceived": true,
        "eventAssigned": true,
        "new": true,
        "taskAssigned": true,
        "updated": true
      },
      "id": "string",
      "lastModified": "string",
      "private": true,
      "products": [
        {}
      ],
      "rating": 1,
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "templateId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access.private` | boolean |  |
| `accountId` | string |  |
| `acl` | array<object> |  |
| `amount` | number |  |
| `assignedTo` | array<object> |  |
| `auxId` | string |  |
| `auxSource` | string |  |
| `auxSourceName` | string |  |
| `closed` | boolean |  |
| `closeDate` | string |  |
| `company` | object |  |
| `contacts` | array<object> |  |
| `createdAt` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.notificationOptIn` | boolean |  |
| `dealProducts` | array<object> |  |
| `description` | string |  |
| `flags.callAssigned` | boolean |  |
| `flags.caseAssigned` | boolean |  |
| `flags.emailReceived` | boolean |  |
| `flags.eventAssigned` | boolean |  |
| `flags.new` | boolean |  |
| `flags.taskAssigned` | boolean |  |
| `flags.updated` | boolean |  |
| `id` | string |  |
| `lastModified` | string |  |
| `private` | boolean |  |
| `products` | array<object> |  |
| `rating` | number |  |
| `tags` | array<object> |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |
| `templateId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `GET /deals/` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

