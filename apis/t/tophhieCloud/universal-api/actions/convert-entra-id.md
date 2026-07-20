# Tophhie Cloud: Convert Entra ID

Converts an Entra ID object ID or SID in Tophhie Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/convert-entra-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/convert-entra-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/convert-entra-id?${params}`, {
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
| `id` | string | yes | The Entra Object ID or SID to convert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "convertDirection": "string",
      "errorMessage": "string",
      "originalId": "string",
      "returnId": "string",
      "support": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `convertDirection` | string | Conversion direction. |
| `errorMessage` | string | Conversion error message when present. |
| `originalId` | string | Original submitted ID. |
| `returnId` | string | Converted ID value. |
| `support` | object | Tophhie Cloud API support details. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /entra/convertid/{id}` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-entra-id.md) for the provider-specific parameters and requirements.

