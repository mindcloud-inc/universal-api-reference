# Figma: Get Published Variables

Retrieves published variables from a Figma file.

```
GET https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-published-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-published-variables?connectionId=$CONNECTION_ID&fileKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-published-variables?${params}`, {
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
| `fileKey` | string | yes | The Figma file key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "meta": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `meta` | object |  |
| `status` | number |  |

## Native endpoint

Through the native Figma API, this operation is `GET /files/:file_key/variables/published` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-published-variables.md) for the provider-specific parameters and requirements.

