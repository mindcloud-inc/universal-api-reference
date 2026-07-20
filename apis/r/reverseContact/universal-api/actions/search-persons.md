# Reverse Contact: Search Persons



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/search-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/search-persons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/search-persons?${params}`, {
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
| `currentCompanyName` | string | no | Filter by the person's current company name. |
| `currentPositionTitle` | string | no | Filter by the person's current job title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentCompanyLinkedinId": "https://example.com",
      "currentCompanyName": "Ava Chen",
      "currentPositionTitle": "string",
      "firstName": "Ava",
      "headline": "string",
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "publicId": "string",
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentCompanyLinkedinId` | string |  |
| `currentCompanyName` | string |  |
| `currentPositionTitle` | string |  |
| `firstName` | string |  |
| `headline` | string |  |
| `lastName` | string |  |
| `linkedinUrl` | string |  |
| `publicId` | string |  |
| `updateDate` | date |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/search/persons` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-persons.md) for the provider-specific parameters and requirements.

