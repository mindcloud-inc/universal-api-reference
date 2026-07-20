# Twenty: Get Person



```
GET https://connect.mindcloud.co/v1/universal/twenty/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/get-person?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twenty/latest/actions/get-person?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarFile": "string",
      "avatarUrl": "https://example.com",
      "city": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "deletedAt": "string",
      "emails": {
        "additionalEmails": [
          "ava@example.com"
        ],
        "primaryEmail": "ava@example.com"
      },
      "id": "string",
      "jobTitle": "string",
      "linkedinLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      },
      "name": {
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "phones": {
        "additionalPhones": [
          "string"
        ],
        "primaryPhoneCallingCode": "string",
        "primaryPhoneCountryCode": "string",
        "primaryPhoneNumber": "string"
      },
      "position": 1,
      "searchVector": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "xLink": {
        "primaryLinkLabel": "https://example.com",
        "primaryLinkUrl": "https://example.com",
        "secondaryLinks": [
          "https://example.com"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarFile` | string |  |
| `avatarUrl` | string |  |
| `city` | string |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `createdBy.name` | string |  |
| `createdBy.source` | string |  |
| `deletedAt` | string |  |
| `emails.additionalEmails` | array<string> |  |
| `emails.primaryEmail` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `linkedinLink.primaryLinkLabel` | string |  |
| `linkedinLink.primaryLinkUrl` | string |  |
| `linkedinLink.secondaryLinks` | array<string> |  |
| `name.firstName` | string |  |
| `name.lastName` | string |  |
| `phones.additionalPhones` | array<string> |  |
| `phones.primaryPhoneCallingCode` | string |  |
| `phones.primaryPhoneCountryCode` | string |  |
| `phones.primaryPhoneNumber` | string |  |
| `position` | number |  |
| `searchVector` | string |  |
| `updatedAt` | date |  |
| `updatedBy.name` | string |  |
| `updatedBy.source` | string |  |
| `xLink.primaryLinkLabel` | string |  |
| `xLink.primaryLinkUrl` | string |  |
| `xLink.secondaryLinks` | array<string> |  |

## Native endpoint

Through the native Twenty API, this operation is `GET /rest/people/:id` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

