# Smartcat: Create Translation Memory

Creates a new translation memory in Smartcat.

```
POST https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/create-translation-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/create-translation-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "sourceLanguage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/create-translation-memory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "sourceLanguage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Translation memory name. |
| `sourceLanguage` | string | yes | Source language code. |
| `targetLanguages[]` | array<string> | no | Target language codes. |
| `description` | string | no | Translation memory description. |
| `clientId` | string | no | Client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tmId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tmId` | string | Created translation memory ID |

## Native endpoint

Through the native Smartcat API, this operation is `POST /api/integration/v1/translationmemory` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-translation-memory.md) for the provider-specific parameters and requirements.

