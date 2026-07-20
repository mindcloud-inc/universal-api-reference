# Stencil: Get Airtable Image Generation Status



```
GET https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-airtable-image-generation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-airtable-image-generation-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-airtable-image-generation-status?${params}`, {
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
| `id` | string | yes | Airtable action ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionTitle": "string",
      "baseId": "string",
      "status": "string",
      "tableName": "Ava Chen",
      "viewName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionTitle` | string |  |
| `baseId` | string |  |
| `status` | string |  |
| `tableName` | string |  |
| `viewName` | string |  |

## Native endpoint

Through the native Stencil API, this operation is `GET /v1/airtables/:id` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-airtable-image-generation-status.md) for the provider-specific parameters and requirements.

