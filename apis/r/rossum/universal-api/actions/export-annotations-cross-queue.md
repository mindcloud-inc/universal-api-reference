# Rossum: Export Annotations Cross-Queue

Exports annotations across Rossum queues.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/export-annotations-cross-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/export-annotations-cross-queue?connectionId=$CONNECTION_ID&annotations%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "annotations[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/export-annotations-cross-queue?${params}`, {
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
| `annotations[]` | array<string> | yes | Annotation URLs to export across queues. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Rossum pagination metadata. |
| `results` | array<object> | Exported annotation rows. |

## Native endpoint

Through the native Rossum API, this operation is `POST /annotations/export` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-annotations-cross-queue.md) for the provider-specific parameters and requirements.

