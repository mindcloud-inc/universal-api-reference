# Crisp: List People Profiles

Retrieves people profiles from Crisp.

```
GET https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-people-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crisp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-people-profiles?connectionId=$CONNECTION_ID&limit=25&offset=0&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crisp/latest/actions/list-people-profiles?${params}`, {
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
| `websiteId` | string | yes | The website identifier |
| `pageNumber` | number | no | Page number for people paging Default: `1`. |
| `perPage` | number | no | Page size for people paging Default: `20`. |
| `sortField` | string | no | Sort on field |
| `sortOrder` | string | no | Sort order |
| `searchOperator` | string | no | Search operator |
| `searchFilter` | string | no | Search filter |
| `searchText` | string | no | Search text |
| `filterDateStart` | date | no | When to start relative to profile creation date |
| `filterDateEnd` | date | no | When to end relative to profile creation date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": {},
      "company": {},
      "createdAt": 1,
      "email": "ava@example.com",
      "peopleId": "string",
      "person": {},
      "segments": [
        "string"
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | object |  |
| `company` | object |  |
| `createdAt` | number |  |
| `email` | string |  |
| `peopleId` | string |  |
| `person` | object |  |
| `segments` | array<string> |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Crisp API, this operation is `GET /website/:website_id/people/profiles/:page_number` (base URL `https://api.crisp.chat/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people-profiles.md) for the provider-specific parameters and requirements.

