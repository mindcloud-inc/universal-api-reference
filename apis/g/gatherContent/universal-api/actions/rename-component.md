# GatherContent: Rename Component

Renames an existing component in GatherContent.

```
PUT https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/rename-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/rename-component" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "component_uuid": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/rename-component', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "component_uuid": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `component_uuid` | string | yes | Component UUID. |
| `name` | string | yes | Component name. |

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

Through the native GatherContent API, this operation is `POST /components/:component_uuid/rename` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-component.md) for the provider-specific parameters and requirements.

