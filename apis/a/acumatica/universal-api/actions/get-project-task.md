# Acumatica: Get Project Task



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-project-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-project-task?connectionId=$CONNECTION_ID&id=f495a825-9b03-4bfc-8844-37094a792142" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "f495a825-9b03-4bfc-8844-37094a792142"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-project-task?${params}`, {
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
| `id` | string | yes | The Acumatica entity ID (GUID) returned in the record's id field. Example: `f495a825-9b03-4bfc-8844-37094a792142`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `ProjectID,ProjectTaskID,Description,Status`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Attributes`. |
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

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ProjectTask/:id` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-task.md) for the provider-specific parameters and requirements.

