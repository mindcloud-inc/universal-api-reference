# SafetyCulture: Get Inspection Details

Retrieves inspection details from SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/get-inspection-details?${params}`, {
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
| `id` | string | yes | The ID for the inspection. |
| `includeMediaUrl` | boolean | no | Whether to include media URLs (and metadata) in the response payload. Optional. Defaults to false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "completedTime": "2026-05-07T12:00:00.000Z",
        "createdTime": "2026-05-07T12:00:00.000Z",
        "inspectionId": "string",
        "inspectionName": "Ava Chen",
        "isMarkedAsComplete": true,
        "lastModifiedTime": "2026-05-07T12:00:00.000Z"
      },
      "template": {
        "templateId": "string",
        "templateName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata.completedTime` | date |  |
| `metadata.createdTime` | date |  |
| `metadata.inspectionId` | string |  |
| `metadata.inspectionName` | string |  |
| `metadata.isMarkedAsComplete` | boolean |  |
| `metadata.lastModifiedTime` | date |  |
| `template.templateId` | string |  |
| `template.templateName` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /inspections/v1/inspections/{id}/details` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inspection-details.md) for the provider-specific parameters and requirements.

