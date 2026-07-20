# Docubee: List Instance Properties

Retrieves properties for a Docubee workflow instance.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-properties?${params}`, {
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
| `instanceId` | string | no | The workflow instance ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedOn": "string",
      "instanceId": "string",
      "startedOn": "string",
      "status": "string",
      "templateId": "string",
      "updatedOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedOn` | string | When the workflow instance completed. |
| `instanceId` | string | The workflow instance ID. |
| `startedOn` | string | When the workflow instance started. |
| `status` | string | The workflow instance status. |
| `templateId` | string | The workflow template ID. |
| `updatedOn` | string | When the workflow instance was last updated. |

## Native endpoint

Through the native Docubee API, this operation is `GET /instances/:instanceId/properties` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-instance-properties.md) for the provider-specific parameters and requirements.

