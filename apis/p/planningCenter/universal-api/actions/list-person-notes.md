# Planning Center: List Person Notes

Retrieves notes for a person in Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-notes?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-notes?${params}`, {
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
| `where.note` | string | no |  |
| `where.noteCategoryId` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no |  |
| `order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdById": "string",
        "displayDate": "2026-05-07T12:00:00.000Z",
        "note": "string",
        "noteCategoryId": "string",
        "organizationId": "string",
        "personId": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {
        "createdBy": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "noteCategory": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
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
| `attributes.createdAt` | date |  |
| `attributes.createdById` | string |  |
| `attributes.displayDate` | date |  |
| `attributes.note` | string |  |
| `attributes.noteCategoryId` | string |  |
| `attributes.organizationId` | string |  |
| `attributes.personId` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `relationships.createdBy.data.id` | string |  |
| `relationships.createdBy.data.type` | string |  |
| `relationships.noteCategory.data.id` | string |  |
| `relationships.noteCategory.data.type` | string |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.person.data.id` | string |  |
| `relationships.person.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/people/:person_id/notes` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-notes.md) for the provider-specific parameters and requirements.

