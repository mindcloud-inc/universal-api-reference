# Salesmate: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-contact?${params}`, {
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
| `contactId` | number | yes | Salesmate contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "description": "string",
      "designation": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isDeleted": true,
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "lastModifiedBy": {},
      "lastName": "Chen",
      "lastNoteAddedBy": {},
      "mobile": "string",
      "name": "Ava Chen",
      "openActivities": 1,
      "openDealCount": 1,
      "owner": {},
      "phone": "string",
      "tags": "string",
      "totalActivities": 1,
      "type": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object | Linked company summary. |
| `createdAt` | date | Creation timestamp. |
| `createdBy` | object | Creator summary. |
| `description` | string | Contact description. |
| `designation` | string | Job title. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `id` | number | Contact ID. |
| `isDeleted` | boolean | Deletion flag. |
| `lastModifiedAt` | date | Last modification timestamp. |
| `lastModifiedBy` | object | Last modifier summary. |
| `lastName` | string | Last name. |
| `lastNoteAddedBy` | object | Last note author summary. |
| `mobile` | string | Mobile phone number. |
| `name` | string | Contact display name. |
| `openActivities` | number | Open activity count. |
| `openDealCount` | number | Open deal count. |
| `owner` | object | Owner summary. |
| `phone` | string | Primary phone number. |
| `tags` | string | Tags. |
| `totalActivities` | number | Total activity count. |
| `type` | string | Salesmate contact type. |
| `website` | string | Website. |

## Native endpoint

Through the native Salesmate API, this operation is `GET /contact/v4/:contactId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

