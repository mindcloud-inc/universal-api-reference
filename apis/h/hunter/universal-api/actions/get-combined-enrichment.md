# Hunter: Get Combined Enrichment



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-combined-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-combined-enrichment?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-combined-enrichment?${params}`, {
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
| `email` | string | yes | Email address to enrich. |
| `clearbitFormat` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "person": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `person` | object |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /combined/find` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-combined-enrichment.md) for the provider-specific parameters and requirements.

