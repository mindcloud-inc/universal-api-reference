# Swipe One: List Tag Contacts



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-tag-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-tag-contacts?connectionId=$CONNECTION_ID&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-tag-contacts?${params}`, {
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
| `tagId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contacts": [
          {
            "createdAt": "string",
            "createdBy": {
              "id": "string",
              "name": "Ava Chen",
              "type": "string"
            },
            "email": "ava@example.com",
            "emailVerificationStatus": "ava@example.com",
            "firstName": "Ava",
            "fullName": "Ava Chen",
            "Id": "string",
            "lastName": "Chen",
            "marketingEmailSubscriptionStatus": "ava@example.com",
            "meta": {
              "count": {
                "lowerBound": 1
              }
            },
            "paginationToken": "string",
            "updatedAt": "string",
            "V": 1,
            "whatsappMarketingConsent": "string",
            "whatsappMessageUndeliverable": true,
            "workspaceId": "string"
          }
        ],
        "count": 1,
        "searchAfter": "string",
        "searchBefore": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.contacts[].createdAt` | string |  |
| `data.contacts[].createdBy.id` | string |  |
| `data.contacts[].createdBy.name` | string |  |
| `data.contacts[].createdBy.type` | string |  |
| `data.contacts[].email` | string |  |
| `data.contacts[].emailVerificationStatus` | string |  |
| `data.contacts[].firstName` | string |  |
| `data.contacts[].fullName` | string |  |
| `data.contacts[].Id` | string |  |
| `data.contacts[].lastName` | string |  |
| `data.contacts[].marketingEmailSubscriptionStatus` | string |  |
| `data.contacts[].meta.count.lowerBound` | number |  |
| `data.contacts[].paginationToken` | string |  |
| `data.contacts[].updatedAt` | string |  |
| `data.contacts[].V` | number |  |
| `data.contacts[].whatsappMarketingConsent` | string |  |
| `data.contacts[].whatsappMessageUndeliverable` | boolean |  |
| `data.contacts[].workspaceId` | string |  |
| `data.count` | number |  |
| `data.searchAfter` | string |  |
| `data.searchBefore` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `GET /tags/:tagId/contacts` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tag-contacts.md) for the provider-specific parameters and requirements.

