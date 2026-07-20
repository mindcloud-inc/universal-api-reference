# Presenton: Export Presentation V3



```
GET https://connect.mindcloud.co/v1/universal/presenton/latest/actions/export-presentation-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/export-presentation-v3?connectionId=$CONNECTION_ID&id=string&exportAs=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "exportAs": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/export-presentation-v3?${params}`, {
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
| `id` | string | yes | The presentation ID to export. |
| `exportAs` | string | yes | Export format such as pptx or pdf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "editPath": "string",
      "path": "string",
      "presentationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number |  |
| `editPath` | string |  |
| `path` | string |  |
| `presentationId` | string |  |

## Native endpoint

Through the native Presenton API, this operation is `POST /api/v3/presentation/export` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-presentation-v3.md) for the provider-specific parameters and requirements.

