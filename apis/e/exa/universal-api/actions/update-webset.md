# Exa: Update Webset

Updates an existing webset in Exa.

```
PUT https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id or externalId of the Webset |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Set of key-value pairs you want to associate with this object. |

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

Through the native Exa API, this operation is `POST /websets/v0/websets/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webset.md) for the provider-specific parameters and requirements.

