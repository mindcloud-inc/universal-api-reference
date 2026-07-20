# Reply: Create New Contact



```
POST https://connect.mindcloud.co/v1/universal/reply/latest/actions/create-new-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reply/latest/actions/create-new-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reply/latest/actions/create-new-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email address. |
| `firstName` | string | yes | Contact first name. |

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

Through the native Reply API, this operation is `POST /v1/people` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-contact.md) for the provider-specific parameters and requirements.

