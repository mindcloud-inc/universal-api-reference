# Hume: List prompt versions



```
GET https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-prompt-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-prompt-versions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-prompt-versions?${params}`, {
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
| `id` | string | yes | EVI prompt identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": 1,
      "id": "string",
      "modifiedOn": 1,
      "name": "Ava Chen",
      "promptExpansion": {},
      "text": "string",
      "version": 1,
      "versionDescription": "string",
      "versionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | number |  |
| `id` | string |  |
| `modifiedOn` | number |  |
| `name` | string |  |
| `promptExpansion` | object |  |
| `text` | string |  |
| `version` | number |  |
| `versionDescription` | string |  |
| `versionType` | string |  |

## Native endpoint

Through the native Hume API, this operation is `GET /v0/evi/prompts/:id` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-prompt-versions.md) for the provider-specific parameters and requirements.

