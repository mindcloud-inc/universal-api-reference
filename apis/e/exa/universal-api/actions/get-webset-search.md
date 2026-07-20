# Exa: Get Webset Search

Retrieves a webset search from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset-search?connectionId=$CONNECTION_ID&webset=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webset": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset-search?${params}`, {
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
| `webset` | string | yes | The id of the Webset |
| `id` | string | yes | The id of the Search |

## Response

```json
{
  "success": true,
  "data": [
    {
      "behavior": "string",
      "canceledAt": "string",
      "canceledReason": "string",
      "count": "string",
      "createdAt": "string",
      "criteria": "string",
      "entity": {
        "description": "string",
        "type": "string"
      },
      "exclude": "string",
      "id": "string",
      "metadata": "string",
      "object": "string",
      "progress": {
        "analyzed": "string",
        "completion": "string",
        "found": "string",
        "timeLeft": "string"
      },
      "query": "string",
      "recall": {},
      "scope": "string",
      "status": "string",
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
| `behavior` | string |  |
| `canceledAt` | string |  |
| `canceledReason` | string |  |
| `count` | string |  |
| `createdAt` | string |  |
| `criteria` | string |  |
| `entity` | object |  |
| `entity.description` | string |  |
| `entity.type` | string |  |
| `exclude` | string |  |
| `id` | string |  |
| `metadata` | string |  |
| `object` | string |  |
| `progress` | object |  |
| `progress.analyzed` | string |  |
| `progress.completion` | string |  |
| `progress.found` | string |  |
| `progress.timeLeft` | string |  |
| `query` | string |  |
| `recall` | object |  |
| `scope` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `websetId` | string |  |

## Native endpoint

Through the native Exa API, this operation is `GET /websets/v0/websets/:webset/searches/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webset-search.md) for the provider-specific parameters and requirements.

