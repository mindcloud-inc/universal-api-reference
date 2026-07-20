# Exa: Delete Webset Enrichment

Deletes an existing webset enrichment from Exa.

```
DELETE https://connect.mindcloud.co/v1/universal/exa/latest/actions/delete-webset-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/exa/latest/actions/delete-webset-enrichment?connectionId=$CONNECTION_ID&webset=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webset": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/delete-webset-enrichment?${params}`, {
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
| `webset` | string | yes | The id or externalId of the Webset |
| `id` | string | yes | The id of the Enrichment |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "format": "string",
      "id": "string",
      "instructions": "string",
      "metadata": "string",
      "object": "string",
      "options": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "string",
      "websetId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `format` | string |  |
| `id` | string |  |
| `instructions` | string |  |
| `metadata` | string |  |
| `object` | string |  |
| `options` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `websetId` | string |  |

## Native endpoint

Through the native Exa API, this operation is `DELETE /websets/v0/websets/:webset/enrichments/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webset-enrichment.md) for the provider-specific parameters and requirements.

