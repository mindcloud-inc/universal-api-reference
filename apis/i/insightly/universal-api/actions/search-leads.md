# Insightly: Search Leads

Finds leads in Insightly by search filters.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-leads?${params}`, {
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
| `fieldName` | string | no | Filter leads by this field name. |
| `fieldValue` | string | no | Filter leads by this field value. |
| `updatedAfterUtc` | string | no | Return leads updated after this UTC timestamp. |
| `brief` | boolean | no | Return only top-level properties for each lead. |
| `countTotal` | boolean | no | Return the total-record count in the response headers. |

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

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Leads/Search` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-leads.md) for the provider-specific parameters and requirements.

