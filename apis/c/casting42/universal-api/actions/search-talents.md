# Casting42: Search Talents

Finds Casting42 talents by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/casting42/latest/actions/search-talents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/search-talents?connectionId=$CONNECTION_ID&query%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/casting42/latest/actions/search-talents?${params}`, {
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
| `limit` | number | no | Maximum number of talents to return. |
| `offset` | number | no | Number of records to skip before returning results. |
| `sortField` | string | no | Field to sort by, such as updatedAt. |
| `sortOrder` | string | no | Sort direction. Use asc or desc. |
| `query[]` | array<object> | yes | Array of search clauses. Each entry is one OR block of field filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "birthday": "string",
      "createdAt": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "hiddenName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "mobilePhone": "string",
      "profilePicture": "string",
      "skills": {},
      "slug": "string",
      "stageName": "Ava Chen",
      "tag": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number | Talent age. |
| `birthday` | string | Talent birthday as returned by Casting42. |
| `createdAt` | string | Talent creation date as returned by Casting42. |
| `customFields` | array<object> | Custom field values returned for the talent. |
| `email` | string | Talent email address. |
| `firstName` | string | Talent first name. |
| `fullName` | string | Full talent name. |
| `hiddenName` | string | Privacy-safe display name. |
| `id` | string | Unique talent ID. |
| `lastName` | string | Talent last name. |
| `mobilePhone` | string | Talent mobile phone number. |
| `profilePicture` | string | Profile picture URL. |
| `skills` | object | Skill groups keyed by Casting42 field labels. |
| `slug` | string | Talent slug. |
| `stageName` | string | Talent stage name. |
| `tag` | string | Talent tag used across Casting42 endpoints. |
| `updatedAt` | string | Talent update date as returned by Casting42. |

## Native endpoint

Through the native Casting42 API, this operation is `POST /api/v2/talents/find` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-talents.md) for the provider-specific parameters and requirements.

