# Swipe One: Search Contacts



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/search-contacts?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/search-contacts?${params}`, {
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
| `workspaceId` | string | yes |  |
| `filter` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contacts": [
          {
            "contactSource": "string",
            "country": "string",
            "createdAt": "string",
            "createdBy": {
              "id": "string",
              "name": "Ava Chen",
              "type": "string"
            },
            "customerLifetimeValue": 1,
            "email": "ava@example.com",
            "emailVerificationStatus": "ava@example.com",
            "fullName": "Ava Chen",
            "Id": "string",
            "jobTitle": "string",
            "lastActivityDate": "string",
            "marketingEmailSubscriptionStatus": "ava@example.com",
            "meta": {
              "count": {
                "lowerBound": 1
              }
            },
            "ordersCount": 1,
            "paginationToken": "string",
            "phone": {
              "countryCode": "string",
              "number": "string"
            },
            "status": "string",
            "tags": [
              "string"
            ],
            "updatedAt": "string",
            "V": 1,
            "website": "string",
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
| `data.contacts[].contactSource` | string |  |
| `data.contacts[].country` | string |  |
| `data.contacts[].createdAt` | string |  |
| `data.contacts[].createdBy.id` | string |  |
| `data.contacts[].createdBy.name` | string |  |
| `data.contacts[].createdBy.type` | string |  |
| `data.contacts[].customerLifetimeValue` | number |  |
| `data.contacts[].email` | string |  |
| `data.contacts[].emailVerificationStatus` | string |  |
| `data.contacts[].fullName` | string |  |
| `data.contacts[].Id` | string |  |
| `data.contacts[].jobTitle` | string |  |
| `data.contacts[].lastActivityDate` | string |  |
| `data.contacts[].marketingEmailSubscriptionStatus` | string |  |
| `data.contacts[].meta.count.lowerBound` | number |  |
| `data.contacts[].ordersCount` | number |  |
| `data.contacts[].paginationToken` | string |  |
| `data.contacts[].phone.countryCode` | string |  |
| `data.contacts[].phone.number` | string |  |
| `data.contacts[].status` | string |  |
| `data.contacts[].tags[]` | string |  |
| `data.contacts[].updatedAt` | string |  |
| `data.contacts[].V` | number |  |
| `data.contacts[].website` | string |  |
| `data.contacts[].whatsappMarketingConsent` | string |  |
| `data.contacts[].whatsappMessageUndeliverable` | boolean |  |
| `data.contacts[].workspaceId` | string |  |
| `data.count` | number |  |
| `data.searchAfter` | string |  |
| `data.searchBefore` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `POST /workspaces/:workspaceId/contacts/search` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

