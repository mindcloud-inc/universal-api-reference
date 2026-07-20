# Swipe One: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contact": {
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
          "ordersCount": 1,
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
| `data.contact.contactSource` | string |  |
| `data.contact.country` | string |  |
| `data.contact.createdAt` | string |  |
| `data.contact.createdBy.id` | string |  |
| `data.contact.createdBy.name` | string |  |
| `data.contact.createdBy.type` | string |  |
| `data.contact.customerLifetimeValue` | number |  |
| `data.contact.email` | string |  |
| `data.contact.emailVerificationStatus` | string |  |
| `data.contact.fullName` | string |  |
| `data.contact.Id` | string |  |
| `data.contact.jobTitle` | string |  |
| `data.contact.lastActivityDate` | string |  |
| `data.contact.marketingEmailSubscriptionStatus` | string |  |
| `data.contact.ordersCount` | number |  |
| `data.contact.phone.countryCode` | string |  |
| `data.contact.phone.number` | string |  |
| `data.contact.status` | string |  |
| `data.contact.tags[]` | string |  |
| `data.contact.updatedAt` | string |  |
| `data.contact.V` | number |  |
| `data.contact.website` | string |  |
| `data.contact.whatsappMarketingConsent` | string |  |
| `data.contact.whatsappMessageUndeliverable` | boolean |  |
| `data.contact.workspaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `GET /contacts/:contactId` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

