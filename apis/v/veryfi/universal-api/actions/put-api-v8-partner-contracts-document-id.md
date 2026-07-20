# Veryfi: Update a Contract

Updates an existing contract in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-contracts-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-contracts-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-contracts-document-id', {
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
      "contract_name": {},
      "created_date": "string",
      "date": {},
      "end_date": {},
      "governing_law": {},
      "id": 1,
      "meta": {},
      "notice_period": {},
      "parties": [
        {}
      ],
      "pdf_url": "https://example.com",
      "renewal_term": {},
      "start_date": {},
      "term": {},
      "termination_for_convenience_period": {},
      "termination_notice": {},
      "text": "string",
      "total": {},
      "updated_date": "string",
      "vanity": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contract_name` | object |  |
| `created_date` | string |  |
| `date` | object |  |
| `end_date` | object |  |
| `governing_law` | object |  |
| `id` | number |  |
| `meta` | object |  |
| `notice_period` | object |  |
| `parties` | array<object> |  |
| `pdf_url` | string |  |
| `renewal_term` | object |  |
| `start_date` | object |  |
| `term` | object |  |
| `termination_for_convenience_period` | object |  |
| `termination_notice` | object |  |
| `text` | string |  |
| `total` | object |  |
| `updated_date` | string |  |
| `vanity` | object |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/contracts/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-contracts-document-id.md) for the provider-specific parameters and requirements.

