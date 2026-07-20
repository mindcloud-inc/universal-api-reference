# Exa: Create Webset

Creates a new webset in Exa.

```
POST https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | object | no | Create initial search for the Webset. |
| `import` | string | no | Attach/load data from existing Imports or Websets into this Webset. For CSV Imports, this schedules ingestion and creates a staging pool of items (ImportItems do not automatically appear as Webset Items; searches create Webset Items). This does not filter searches. To filter a search to only look within an Import or Webset, use search.scope instead. |
| `enrichments` | string | no | Add enrichments to extract additional data from found items. Enrichments automatically search for and extract specific information (like contact details, funding data, employee counts, etc.) from each item added to your Webset. |
| `exclude` | string | no | Global exclusion sources (existing imports or websets) that apply to all operations within this Webset. Any results found within these sources will be omitted across all search and import operations. |
| `externalId` | string | no | The external identifier for the webset. You can use this to reference the Webset by your own internal identifiers. |
| `metadata` | string | no | Set of key-value pairs you want to associate with this object. |

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
| `metadata` | string |  |
| `monitors` | string |  |
| `object` | string |  |
| `searches` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Exa API, this operation is `POST /websets/v0/websets` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webset.md) for the provider-specific parameters and requirements.

