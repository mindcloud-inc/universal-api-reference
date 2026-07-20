# Planning Center: List Person Emails

Retrieves email addresses for a person in Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-emails?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-emails?${params}`, {
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
| `personId` | string | yes |  |
| `where.address` | string | no |  |
| `where.blocked` | boolean | no |  |
| `where.createdAt` | date | no |  |
| `where.location` | string | no |  |
| `where.primary` | boolean | no |  |
| `where.updatedAt` | date | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "address": "string",
        "blocked": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "location": "string",
        "primary": true,
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {
        "person": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.address` | string |  |
| `attributes.blocked` | boolean |  |
| `attributes.createdAt` | date |  |
| `attributes.location` | string |  |
| `attributes.primary` | boolean |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `relationships.person.data.id` | string |  |
| `relationships.person.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/people/:person_id/emails` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-emails.md) for the provider-specific parameters and requirements.

