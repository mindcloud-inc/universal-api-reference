# BuildBetter: Create Person



```
POST https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "alex@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "alex@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Person email address. Example: `alex@example.com`. |
| `firstName` | string | no | Person first name. Example: `Alex`. |
| `lastName` | string | no | Person last name. Example: `Johnson`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Link this person to an existing company ID. Example: `12345`. |
| `title` | string | no | Person job title. Example: `Sales Leader`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "company_id": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object | Linked company summary. |
| `company_id` | string | Linked company identifier. |
| `email` | string | Person email address. |
| `first_name` | string | Person first name. |
| `id` | string | BuildBetter person identifier. |
| `last_name` | string | Person last name. |
| `title` | string | Person job title. |
| `updated_at` | date | Last updated timestamp. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

