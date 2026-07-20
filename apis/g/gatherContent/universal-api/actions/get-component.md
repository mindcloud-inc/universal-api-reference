# GatherContent: Get Component

Retrieves a component from GatherContent.

```
GET https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-component?connectionId=$CONNECTION_ID&component_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "component_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-component?${params}`, {
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
| `component_uuid` | string | yes | Component UUID. |

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

Through the native GatherContent API, this operation is `GET /components/:component_uuid` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-component.md) for the provider-specific parameters and requirements.

