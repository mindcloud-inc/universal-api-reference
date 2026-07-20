# Smoove: List Landing Page Recipients

Retrieves subscribers for a Smoove landing page.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-landing-page-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-landing-page-recipients?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-landing-page-recipients?${params}`, {
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
| `id` | string | yes |  |
| `fields` | string | no |  |
| `includeCustomFields` | boolean | no |  |
| `includeLinkedLists` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "address": "string",
        "c_DaysSinceSignup": 1,
        "campaignSource": "string",
        "canReceiveEmails": true,
        "canReceiveSmsMessages": true,
        "cellPhone": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "dateOfBirth": "2026-05-07T12:00:00.000Z",
        "deleted": true,
        "email": "ava@example.com",
        "externalId": "string",
        "firstName": "Ava",
        "id": 1,
        "ipSignup": "string",
        "joinSource": "string",
        "lastChanged": "2026-05-07T12:00:00.000Z",
        "lastName": "Chen",
        "listAssociationTime": "2026-05-07T12:00:00.000Z",
        "phone": "string",
        "position": "string",
        "timestampSignup": "2026-05-07T12:00:00.000Z",
        "timestampUnsubscribed": "2026-05-07T12:00:00.000Z",
        "unsubscribeReasonComment": "string",
        "unsubscribeReasonType": "string"
      },
      "contactId": 1,
      "id": 1,
      "pageUrl": "https://example.com",
      "timeStamp": "2026-05-07T12:00:00.000Z",
      "userIP": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.address` | string |  |
| `contact.c_DaysSinceSignup` | number |  |
| `contact.campaignSource` | string |  |
| `contact.canReceiveEmails` | boolean |  |
| `contact.canReceiveSmsMessages` | boolean |  |
| `contact.cellPhone` | string |  |
| `contact.city` | string |  |
| `contact.company` | string |  |
| `contact.country` | string |  |
| `contact.dateOfBirth` | date |  |
| `contact.deleted` | boolean |  |
| `contact.email` | string |  |
| `contact.externalId` | string |  |
| `contact.firstName` | string |  |
| `contact.id` | number |  |
| `contact.ipSignup` | string |  |
| `contact.joinSource` | string |  |
| `contact.lastChanged` | date |  |
| `contact.lastName` | string |  |
| `contact.listAssociationTime` | date |  |
| `contact.phone` | string |  |
| `contact.position` | string |  |
| `contact.timestampSignup` | date |  |
| `contact.timestampUnsubscribed` | date |  |
| `contact.unsubscribeReasonComment` | string |  |
| `contact.unsubscribeReasonType` | string |  |
| `contactId` | number |  |
| `id` | number |  |
| `pageUrl` | string |  |
| `timeStamp` | date |  |
| `userIP` | string |  |

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/LandingPages/:id/Recipients` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-landing-page-recipients.md) for the provider-specific parameters and requirements.

