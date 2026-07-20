# Planning Center: Create Household Membership

Creates a household membership in Planning Center.

```
POST https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-household-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-household-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "householdId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-household-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "householdId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `householdId` | string | yes | The household id. |
| `data` | object | yes | JSON:API data object for the request payload. |
| `include` | string | no | Include the associated household or person in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "householdRole": "string",
        "pending": true,
        "personName": "Ava Chen"
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
| `attributes.householdRole` | string |  |
| `attributes.pending` | boolean |  |
| `attributes.personName` | string |  |
| `id` | string |  |
| `relationships.person.data.id` | string |  |
| `relationships.person.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `POST /people/v2/households/:household_id/household_memberships` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-household-membership.md) for the provider-specific parameters and requirements.

