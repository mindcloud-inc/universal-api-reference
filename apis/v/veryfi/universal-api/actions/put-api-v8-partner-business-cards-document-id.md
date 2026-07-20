# Veryfi: Update a Business Card

Updates an existing business card in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-business-cards-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-business-cards-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-business-cards-document-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `externalId` | string | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | string | no | Possible values: non-empty Possible values: non-empty Default value: `` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "created_date": "string",
      "email": {},
      "external_id": "string",
      "fax": {},
      "faxes": [
        {}
      ],
      "id": 1,
      "logo_url": {},
      "meta": {},
      "mobile": {},
      "organization": {},
      "parsed_address": {},
      "parsed_name": {},
      "person": {},
      "phone": {},
      "phones": [
        {}
      ],
      "text": "string",
      "title": {},
      "updated_date": "string",
      "web": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `created_date` | string |  |
| `email` | object |  |
| `external_id` | string |  |
| `fax` | object |  |
| `faxes` | array<object> |  |
| `id` | number |  |
| `logo_url` | object |  |
| `meta` | object |  |
| `mobile` | object |  |
| `organization` | object |  |
| `parsed_address` | object |  |
| `parsed_name` | object |  |
| `person` | object |  |
| `phone` | object |  |
| `phones` | array<object> |  |
| `text` | string |  |
| `title` | object |  |
| `updated_date` | string |  |
| `web` | object |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/business-cards/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-business-cards-document-id.md) for the provider-specific parameters and requirements.

