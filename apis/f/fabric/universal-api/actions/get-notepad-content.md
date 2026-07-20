# Fabric: Get Notepad Content

Retrieves notepad content from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-notepad-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-notepad-content?connectionId=$CONNECTION_ID&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-notepad-content?${params}`, {
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
| `resourceId` | string | yes | The notepad resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/notepads/{resourceId}/content` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notepad-content.md) for the provider-specific parameters and requirements.

