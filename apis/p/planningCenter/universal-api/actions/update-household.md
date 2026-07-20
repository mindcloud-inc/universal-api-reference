# Planning Center: Update Household

Updates an existing household in Planning Center.

```
PUT https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/update-household
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/update-household" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/update-household', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The household id. |
| `data` | object | yes | JSON:API data object for the request payload. |
| `include` | string | no | Include associated people in the response. |

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

Through the native Planning Center API, this operation is `PATCH /people/v2/households/:id` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-household.md) for the provider-specific parameters and requirements.

