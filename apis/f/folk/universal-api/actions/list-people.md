# folk: List People

Retrieves a list of people from folk.

```
GET https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-people?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        "string"
      ],
      "birthday": "2026-05-07T12:00:00.000Z",
      "companies": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "customFieldValues": {},
      "description": "string",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "groups": [
        {}
      ],
      "id": "string",
      "interactionMetadata": {},
      "jobTitle": "string",
      "lastName": "Chen",
      "phones": [
        "string"
      ],
      "strongestConnection": {},
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<string> | Addresses |
| `birthday` | date | Birthday |
| `companies` | array<object> | Companies linked to the person |
| `createdAt` | date | Created timestamp |
| `createdBy` | object | User who created the person |
| `customFieldValues` | object | Custom field values by group |
| `description` | string | Person description |
| `emails` | array<string> | Email addresses |
| `firstName` | string | First name |
| `fullName` | string | Full name |
| `groups` | array<object> | Groups linked to the person |
| `id` | string | Person ID |
| `interactionMetadata` | object | Interaction counts and timestamps |
| `jobTitle` | string | Job title |
| `lastName` | string | Last name |
| `phones` | array<string> | Phone numbers |
| `strongestConnection` | object | Strongest connection data |
| `urls` | array<string> | Profile URLs |

## Native endpoint

Through the native folk API, this operation is `GET /v1/people` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

