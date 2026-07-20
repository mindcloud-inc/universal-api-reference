# Recruitee ATS: List Locations



```
GET https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-locations?${params}`, {
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
| `query` | string | no | Search query for locations. |
| `scope` | string | no | Location scope filter. |
| `viewMode` | string | no | View mode filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": {},
      "city": "string",
      "countryCode": "string",
      "createdAt": "string",
      "fullAddress": "string",
      "id": 1,
      "isValid": true,
      "langCode": "string",
      "name": "Ava Chen",
      "note": {},
      "postalCode": {},
      "stateCode": "string",
      "stateName": "Ava Chen",
      "street": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | object |  |
| `city` | string |  |
| `countryCode` | string |  |
| `createdAt` | string |  |
| `fullAddress` | string |  |
| `id` | number |  |
| `isValid` | boolean |  |
| `langCode` | string |  |
| `name` | string |  |
| `note` | object |  |
| `postalCode` | object |  |
| `stateCode` | string |  |
| `stateName` | string |  |
| `street` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `GET /c/:company_id/locations` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

