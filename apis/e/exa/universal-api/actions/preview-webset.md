# Exa: Preview Webset

Retrieves a webset preview from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/preview-webset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/preview-webset?connectionId=$CONNECTION_ID&search=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/preview-webset?${params}`, {
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
| `search` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enrichments": "string",
      "items": "string",
      "search": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enrichments` | string |  |
| `items` | string |  |
| `search` | object |  |

## Native endpoint

Through the native Exa API, this operation is `POST /websets/v0/websets/preview` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-webset.md) for the provider-specific parameters and requirements.

