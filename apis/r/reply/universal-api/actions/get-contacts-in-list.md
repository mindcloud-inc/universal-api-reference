# Reply: Get Contacts In List



```
GET https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-contacts-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-contacts-in-list?connectionId=$CONNECTION_ID&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-contacts-in-list?${params}`, {
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
| `listId` | number | yes | Reply list identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "addingDate": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "company": "string",
      "companySize": "string",
      "country": "string",
      "creationSource": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "industry": "string",
      "lastName": "Chen",
      "linkedInProfile": "https://example.com",
      "linkedInRecruiterUrl": "https://example.com",
      "phone": "string",
      "phoneStatus": "string",
      "salesNavigatorUrl": "https://example.com",
      "state": "string",
      "timeZoneId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `addingDate` | date |  |
| `city` | string |  |
| `company` | string |  |
| `companySize` | string |  |
| `country` | string |  |
| `creationSource` | string |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `industry` | string |  |
| `lastName` | string |  |
| `linkedInProfile` | string |  |
| `linkedInRecruiterUrl` | string |  |
| `phone` | string |  |
| `phoneStatus` | string |  |
| `salesNavigatorUrl` | string |  |
| `state` | string |  |
| `timeZoneId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Reply API, this operation is `GET /v1/people/list/:listId` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contacts-in-list.md) for the provider-specific parameters and requirements.

