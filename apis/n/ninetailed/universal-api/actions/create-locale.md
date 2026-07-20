# Ninetailed: Create Locale



```
POST https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/create-locale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/create-locale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "environmentId": "string",
  "name": "Ava Chen",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/create-locale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "environmentId": "string",
    "name": "Ava Chen",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID. |
| `name` | string | yes | Human-readable locale name. |
| `code` | string | yes | Locale code, for example en-GB. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fallbackCode` | string | no | Fallback locale code, or null when no fallback should apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "default": true,
      "fallbackCode": "string",
      "name": "Ava Chen",
      "sys": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `default` | boolean |  |
| `fallbackCode` | string |  |
| `name` | string |  |
| `sys` | object |  |

## Native endpoint

Through the native Ninetailed API, this operation is `POST /spaces/:space_id/environments/:environment_id/locales` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-locale.md) for the provider-specific parameters and requirements.

