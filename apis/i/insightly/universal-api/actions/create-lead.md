# Insightly: Create Lead

Creates a new lead in Insightly.

```
POST https://connect.mindcloud.co/v1/universal/insightly/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lastName": "Chen",
  "leadSourceId": 1,
  "leadStatusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightly/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lastName": "Chen",
    "leadSourceId": 1,
    "leadStatusId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | The lead's first name. |
| `lastName` | string | yes | The lead's last name. |
| `leadSourceId` | number | yes | The Lead Source ID. |
| `leadStatusId` | number | yes | The Lead Status ID. |
| `email` | string | no | The lead's email address. |
| `phone` | string | no | The lead's phone number. |
| `title` | string | no | The lead's job title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "converted": true,
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailOptedOut": true,
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "leadId": 1,
      "leadSourceId": 1,
      "leadStatusId": 1,
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "organisationName": "Ava Chen",
      "ownerUserId": 1,
      "phone": "string",
      "responsibleUserId": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `converted` | boolean |  |
| `createdUserId` | number |  |
| `dateCreatedUtc` | date |  |
| `dateUpdatedUtc` | date |  |
| `email` | string |  |
| `emailOptedOut` | boolean |  |
| `firstName` | string |  |
| `imageUrl` | string |  |
| `lastActivityDateUtc` | date |  |
| `lastName` | string |  |
| `leadId` | number |  |
| `leadSourceId` | number |  |
| `leadStatusId` | number |  |
| `nextActivityDateUtc` | date |  |
| `organisationName` | string |  |
| `ownerUserId` | number |  |
| `phone` | string |  |
| `responsibleUserId` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Insightly API, this operation is `POST {{credentials.apiBaseUrl}}Leads` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

