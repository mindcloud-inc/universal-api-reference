# Harvestr.io: Update Discovery



```
PUT https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-discovery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-discovery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-discovery', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier (id or clientId) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `discoveryStateId` | string | no | The discovery state ID to set |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": "string",
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "discoveryStateId": "string",
      "fieldsValues": {
        "field": {
          "clientId": "string",
          "id": "string",
          "name": "Ava Chen"
        },
        "value": "string"
      },
      "id": "string",
      "lastDiscoverystateUpdatedAt": "2026-05-07T12:00:00.000Z",
      "lastFeedback": "2026-05-07T12:00:00.000Z",
      "parentId": "string",
      "parentType": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | string | Identifier of the assignee |
| `clientId` | string | Client identifier |
| `createdAt` | date | Creation date of the discovery |
| `description` | string | Description of the discovery |
| `discoveryStateId` | string | Identifier of the discovery state |
| `fieldsValues` | array<object> | Field values for this discovery. Only included when select=discoveryfields is specified in query parameters. |
| `fieldsValues.field` | object | The discovery field definition |
| `fieldsValues.field.clientId` | string | Client identifier |
| `fieldsValues.field.id` | string | Unique identifier of the discovery field |
| `fieldsValues.field.name` | string | Name of the discovery field |
| `fieldsValues.value` | string | Value of the field |
| `id` | string | Unique identifier of the discovery |
| `lastDiscoverystateUpdatedAt` | date | Date when the discovery state was last updated |
| `lastFeedback` | date | Date of the last feedback |
| `parentId` | string | Identifier of the parent (component or discovery) |
| `parentType` | string | Type of the parent entity |
| `tags` | array<string> | Tags associated with this discovery |
| `title` | string | Title of the discovery |
| `updatedAt` | date | Last update date of the discovery |

## Native endpoint

Through the native Harvestr.io API, this operation is `PATCH /discovery/{id}` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-discovery.md) for the provider-specific parameters and requirements.

