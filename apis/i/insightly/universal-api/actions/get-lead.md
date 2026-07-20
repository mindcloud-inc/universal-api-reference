# Insightly: Get Lead

Retrieves a lead from Insightly by ID.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-lead?connectionId=$CONNECTION_ID&leadId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-lead?${params}`, {
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
| `leadId` | number | yes | The Lead ID. |

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

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Leads/:leadId` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

