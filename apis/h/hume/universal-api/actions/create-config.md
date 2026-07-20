# Hume: Create config



```
POST https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "eviVersion": "3",
  "voice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hume/latest/actions/create-config', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "eviVersion": "3",
    "voice": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Config name. |
| `eviVersion` | string | yes | EVI version to use. Supported values include 3 and 4-mini. Default: `3`. |
| `voice` | object | yes | Voice reference object, for example {"provider":"HUME_AI","name":"Ava Song"}. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `versionDescription` | string | no | Optional config version description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": 1,
      "eviVersion": "string",
      "id": "string",
      "modifiedOn": 1,
      "name": "Ava Chen",
      "prompt": {},
      "tools": [
        [
          {}
        ]
      ],
      "version": 1,
      "versionDescription": "string",
      "voice": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | number |  |
| `eviVersion` | string |  |
| `id` | string |  |
| `modifiedOn` | number |  |
| `name` | string |  |
| `prompt` | object |  |
| `tools[]` | array<object> |  |
| `version` | number |  |
| `versionDescription` | string |  |
| `voice` | object |  |

## Native endpoint

Through the native Hume API, this operation is `POST /v0/evi/configs` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-config.md) for the provider-specific parameters and requirements.

