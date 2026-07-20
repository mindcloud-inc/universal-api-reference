# Planning Center: List Households

Retrieves households from Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-households
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-households?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-households?${params}`, {
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
| `include` | string | no | Include associated people in the response. |
| `order` | string | no | Sort households by a supported field; prefix the field with a hyphen for descending order. |
| `where` | object | no | Field-qualified household query filters. |
| `where.createdAt` | date | no | Query households by an exact created_at timestamp in ISO 8601 format. |
| `where.memberCount` | number | no | Query households by an exact member_count value. |
| `where.name` | string | no | Query households by an exact household name. |
| `where.primaryContactName` | string | no | Query households by an exact primary_contact_name value. |
| `where.updatedAt` | date | no | Query households by an exact updated_at timestamp in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "avatar": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "memberCount": 1,
        "name": "Ava Chen",
        "primaryContactId": "string",
        "primaryContactName": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {
        "people": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        },
        "primaryContact": {
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
| `attributes.avatar` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.memberCount` | number |  |
| `attributes.name` | string |  |
| `attributes.primaryContactId` | string |  |
| `attributes.primaryContactName` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `relationships.people.data[].id` | string |  |
| `relationships.people.data[].type` | string |  |
| `relationships.primaryContact.data.id` | string |  |
| `relationships.primaryContact.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/households` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-households.md) for the provider-specific parameters and requirements.

