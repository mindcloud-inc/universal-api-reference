# GatherContent: Create Component

Creates a new component in GatherContent.

```
POST https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/create-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/create-component" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields[]": [
    {}
  ],
  "name": "Ava Chen",
  "project_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/create-component', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields[]": [{}],
    "name": "Ava Chen",
    "project_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[]` | array<object> | yes | Component fields definition. |
| `name` | string | yes | Component name. |
| `project_id` | string | yes | Project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ],
      "name": "Ava Chen",
      "project_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> |  |
| `name` | string |  |
| `project_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native GatherContent API, this operation is `POST /projects/:project_id/components` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-component.md) for the provider-specific parameters and requirements.

