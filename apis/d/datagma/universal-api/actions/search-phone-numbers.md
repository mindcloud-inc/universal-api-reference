# Datagma: Search Phone Numbers

Finds phone numbers in Datagma by email or profile.

```
GET https://connect.mindcloud.co/v1/universal/datagma/latest/actions/search-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datagma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/search-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/search-phone-numbers?${params}`, {
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
| `username` | string | no | Social profile URL or username used as the starting point for phone lookup. |
| `email` | string | no | Email address used as the starting point for phone lookup. |
| `minimum_match` | string | no | Minimum match threshold for the phone search. |
| `whatsapp_check` | string | no | Set true to verify whether a matched number is linked to WhatsApp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableData": {},
      "availableSources": 1,
      "creditBurn": 1,
      "httpStatusCode": 1,
      "person": {},
      "personsCount": 1,
      "possible_persons": [
        {}
      ],
      "query": {},
      "visibleSources": 1,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableData` | object |  |
| `availableSources` | number |  |
| `creditBurn` | number |  |
| `httpStatusCode` | number |  |
| `person` | object |  |
| `personsCount` | number |  |
| `possible_persons` | array<object> |  |
| `query` | object |  |
| `visibleSources` | number |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Datagma API, this operation is `GET /v1/search` (base URL `https://gateway.datagma.net/api/ingress`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-phone-numbers.md) for the provider-specific parameters and requirements.

