# Columns AI: Download Graph Image

Downloads a graph image from Columns AI by visual ID.

```
GET https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/download-graph-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Columns AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/download-graph-image?connectionId=$CONNECTION_ID&id=U6tALuJ3cTdPFw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "U6tALuJ3cTdPFw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/download-graph-image?${params}`, {
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
| `id` | string | yes | Columns visual ID whose image should be downloaded. Example: `U6tALuJ3cTdPFw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | PNG byte array returned from Columns. |
| `type` | string | Raw binary container type returned by the runtime for the image response. |

## Native endpoint

Through the native Columns AI API, this operation is `GET /sdk/image/:id` (base URL `https://columns.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-graph-image.md) for the provider-specific parameters and requirements.

