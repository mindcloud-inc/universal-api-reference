# Exa: Get Webset

Retrieves a webset from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset?${params}`, {
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
| `id` | string | yes | The id or externalId of the Webset. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expand[]` | array<string> | no | Expand the response with the specified resources |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "enrichments": "string",
      "excludes": "string",
      "externalId": "string",
      "id": "string",
      "imports": "string",
      "items": "string",
      "metadata": "string",
      "monitors": "string",
      "object": "string",
      "searches": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `enrichments` | string |  |
| `excludes` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `imports` | string |  |
| `items` | string |  |
| `metadata` | string |  |
| `monitors` | string |  |
| `object` | string |  |
| `searches` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Exa API, this operation is `GET /websets/v0/websets/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webset.md) for the provider-specific parameters and requirements.

