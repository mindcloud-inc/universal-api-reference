# GrowthBook: Create a single archetype

Creates a new archetype in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-archetype
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-archetype" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "isPublic": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-archetype', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "isPublic": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Default: `sample`. |
| `description` | string | no |  |
| `isPublic` | boolean | yes | Whether to make this Archetype available to other team members Default: `true`. |
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

Through the native GrowthBook API, this operation is `POST /archetypes` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-archetype.md) for the provider-specific parameters and requirements.

