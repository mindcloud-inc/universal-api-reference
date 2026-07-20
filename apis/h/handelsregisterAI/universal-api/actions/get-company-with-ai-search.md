# Handelsregister AI: Get Company With AI Search

Retrieves a company using AI search in Handelsregister AI.

```
GET https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/get-company-with-ai-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handelsregister AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/get-company-with-ai-search?connectionId=$CONNECTION_ID&q=BMW%20AG" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "BMW AG"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/get-company-with-ai-search?${params}`, {
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
| `q` | string | yes | Company name, registration number, or search query. Example: `BMW AG`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "contact_data": {},
      "entity_id": "string",
      "industry_classification": {},
      "keywords": [
        "string"
      ],
      "legal_form": "string",
      "meta": {},
      "name": "Ava Chen",
      "products_and_services": [
        "string"
      ],
      "purpose": "string",
      "registration": {},
      "registration_date": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `contact_data` | object |  |
| `entity_id` | string |  |
| `industry_classification` | object |  |
| `keywords` | array<string> |  |
| `legal_form` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `products_and_services` | array<string> |  |
| `purpose` | string |  |
| `registration` | object |  |
| `registration_date` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Handelsregister AI API, this operation is `GET /fetch-organization` (base URL `https://handelsregister.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-with-ai-search.md) for the provider-specific parameters and requirements.

