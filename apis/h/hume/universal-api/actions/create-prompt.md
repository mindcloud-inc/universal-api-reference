# Hume: Create prompt



```
POST https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-prompt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Prompt name. |
| `text` | string | yes | Prompt instructions text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `versionDescription` | string | no | Optional prompt version description. |

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

Through the native Hume API, this operation is `POST /v0/evi/prompts` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prompt.md) for the provider-specific parameters and requirements.

