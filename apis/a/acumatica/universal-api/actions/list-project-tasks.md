# Acumatica: List Project Tasks



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-project-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-project-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-project-tasks?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `ProjectID,ProjectTaskID,Description,Status`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Attributes`. |
| `filter` | string | no | Acumatica OData filter expression used to qualify returned records. Example: `Status eq 'Active'`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `ProjectTaskID,Description`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "files:put": "https://example.com",
        "self": "https://example.com"
      },
      "Default": {
        "value": true
      },
      "Description": {
        "value": "string"
      },
      "id": "string",
      "LastModifiedDateTime": {
        "value": "string"
      },
      "note": {
        "value": "string"
      },
      "ProjectID": {
        "value": "string"
      },
      "ProjectTaskID": {
        "value": "string"
      },
      "rowNumber": 1,
      "Status": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.files:put` | string |  |
| `_links.self` | string |  |
| `Default.value` | boolean |  |
| `Description.value` | string |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | string |  |
| `note.value` | string |  |
| `ProjectID.value` | string |  |
| `ProjectTaskID.value` | string |  |
| `rowNumber` | number |  |
| `Status.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ProjectTask` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-tasks.md) for the provider-specific parameters and requirements.

