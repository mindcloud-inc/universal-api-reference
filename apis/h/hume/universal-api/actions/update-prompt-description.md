# Hume: Update prompt description



```
PUT https://connect.mindcloud.co/v1/universal/hume/latest/actions/update-prompt-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hume/latest/actions/update-prompt-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "version": 1,
  "versionDescription": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hume/latest/actions/update-prompt-description', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "version": 1,
    "versionDescription": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | EVI prompt identifier. |
| `version` | number | yes | Version number. |
| `versionDescription` | string | yes | Updated prompt version description. |

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

Through the native Hume API, this operation is `PATCH /v0/evi/prompts/:id/version/:version` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prompt-description.md) for the provider-specific parameters and requirements.

