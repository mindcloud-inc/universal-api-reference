# Implisense: Get Suggestions

Finds suggestions in Implisense API by prefix.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-suggestions?connectionId=$CONNECTION_ID&prefix=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prefix": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-suggestions?${params}`, {
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
| `prefix` | string | yes | Text prefix to use for Implisense suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "prefix": "string",
      "suggestions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `prefix` | string |  |
| `suggestions` | object |  |

## Native endpoint

Through the native Implisense API, this operation is `GET /suggest/:prefix` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suggestions.md) for the provider-specific parameters and requirements.

