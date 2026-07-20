# Datagma: Enrich a person or a company

Retrieves person or company enrichment data from Datagma.

```
GET https://connect.mindcloud.co/v1/universal/datagma/latest/actions/enrich-a-person-or-a-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datagma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/enrich-a-person-or-a-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/enrich-a-person-or-a-company?${params}`, {
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
| `data` | string | no | Primary enrichment input such as a company name, domain, website, SIREN number, LinkedIn URL, or email address. |
| `full_name` | string | no | Target person's full name when enriching a person. |
| `phone_full` | string | no | Set true to find a mobile phone number from a full name and company name. |
| `company_premium` | string | no | Include basic company information in the response. |
| `company_full` | string | no | Include extended company information in the response. |
| `whatsapp_check` | string | no | Set true to verify whether a found number is linked to WhatsApp. |
| `debug` | string | no | Set false to allow broader scoring results; defaults to false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "creditBurn": "string",
      "email": {},
      "emailV2": {},
      "person": {},
      "phone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `creditBurn` | string |  |
| `email` | object |  |
| `emailV2` | object |  |
| `person` | object |  |
| `phone` | object |  |

## Native endpoint

Through the native Datagma API, this operation is `GET /v2/full` (base URL `https://gateway.datagma.net/api/ingress`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-a-person-or-a-company.md) for the provider-specific parameters and requirements.

