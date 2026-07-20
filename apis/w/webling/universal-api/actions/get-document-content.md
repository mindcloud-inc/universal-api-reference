# Webling: Get Document Content



```
GET https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-document-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-document-content?connectionId=$CONNECTION_ID&id=1&filename=Ava%20Chen&extension=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "filename": "Ava Chen",
  "extension": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-document-content?${params}`, {
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
| `id` | number | yes | Document ID to download. |
| `filename` | string | yes | File name without extension. |
| `extension` | string | yes | File extension. |

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
| `data` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native Webling API, this operation is `GET /document/:id/file/:filename.:extension` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-content.md) for the provider-specific parameters and requirements.

