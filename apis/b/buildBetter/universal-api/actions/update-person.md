# BuildBetter: Update Person



```
PUT https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | BuildBetter person ID. Example: `12345`. |
| `firstName` | string | no | Updated first name. Example: `Alex`. |
| `lastName` | string | no | Updated last name. Example: `Johnson`. |
| `email` | string | no | Updated email address. Example: `alex@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Updated linked company ID. Example: `12345`. |

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

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

