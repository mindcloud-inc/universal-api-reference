# SimpleLocalize: Get Translation Key Details

Retrieves translation key details from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-translation-key-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-translation-key-details?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-translation-key-details?${params}`, {
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
| `key` | string | yes |  |
| `namespace` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charactersLimit": 1,
      "codeDescription": "string",
      "createdAt": "string",
      "createdSource": "string",
      "description": "string",
      "key": "string",
      "lastSeenAt": "string",
      "lastSeenSource": "string",
      "namespace": "Ava Chen",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charactersLimit` | number |  |
| `codeDescription` | string |  |
| `createdAt` | string |  |
| `createdSource` | string |  |
| `description` | string |  |
| `key` | string |  |
| `lastSeenAt` | string |  |
| `lastSeenSource` | string |  |
| `namespace` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v1/translation-keys/details` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-translation-key-details.md) for the provider-specific parameters and requirements.

