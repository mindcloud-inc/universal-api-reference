# GrowthBook: Update a single archetype

Updates an existing archetype in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-archetype
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-archetype" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-archetype', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |
| `name` | string | no |  |
| `description` | string | no |  |
| `isPublic` | boolean | no | Whether to make this Archetype available to other team members |
| `attributes` | object | no | The attributes to set when using this Archetype |
| `projects` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archetype": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archetype` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `PUT /archetypes/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-archetype.md) for the provider-specific parameters and requirements.

