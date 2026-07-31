# Insult API: Get Insult JSON



```
GET https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-insult-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insult API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-insult-json?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insultAPI/latest/actions/get-insult-json?${params}`, {
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
| `lang` | string | no |  |
| `plural` | string | no |  |
| `template` | string | no |  |
| `who` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "args": {},
      "error": true,
      "error_message": "string",
      "insult": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `args` | object |  |
| `error` | boolean |  |
| `error_message` | string |  |
| `insult` | string |  |

## Native endpoint

Through the native Insult API API, this operation is `GET /insult.json` (base URL `https://insult.mattbas.org/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-insult-json.md) for the provider-specific parameters and requirements.

