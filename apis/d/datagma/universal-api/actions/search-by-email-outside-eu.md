# Datagma: Search By Email (outside EU)

Finds contacts in Datagma by email outside the EU.

```
GET https://connect.mindcloud.co/v1/universal/datagma/latest/actions/search-by-email-outside-eu
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datagma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/search-by-email-outside-eu?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/search-by-email-outside-eu?${params}`, {
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
| `email` | string | no | Target email address to search by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "miscellaneous": {},
      "networkingHighlights": {},
      "personalInformation": {},
      "positions": {},
      "schools": {},
      "skillsAndEndorsements": {},
      "userGeneratedContents": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `miscellaneous` | object |  |
| `networkingHighlights` | object |  |
| `personalInformation` | object |  |
| `positions` | object |  |
| `schools` | object |  |
| `skillsAndEndorsements` | object |  |
| `userGeneratedContents` | object |  |

## Native endpoint

Through the native Datagma API, this operation is `GET /v1/reverse_email` (base URL `https://gateway.datagma.net/api/ingress`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-by-email-outside-eu.md) for the provider-specific parameters and requirements.

