# Veryfi: Update a W-2

Updates an existing W-2 in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w2s-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w2s-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w2s-document-id', {
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
      "advance_eic_payment": {},
      "allocated_tips": {},
      "control_number": {},
      "created_date": "string",
      "dependent_care_benefits": {},
      "ein": {},
      "employee_address": {},
      "employee_name": {},
      "employee_ssn": {},
      "employer_address": {},
      "employer_name": {},
      "external_id": "string",
      "federal_income_tax": {},
      "field_12a_col1": {},
      "field_12a_col2": {},
      "field_12b_col1": {},
      "field_12b_col2": {},
      "field_12c_col1": {},
      "field_12c_col2": {},
      "field_12d_col1": {},
      "field_12d_col2": {},
      "field_14_other": [
        {}
      ],
      "id": 1,
      "img_thumbnail_url": "https://example.com",
      "is_13a": {},
      "is_13b": {},
      "is_13c": {},
      "medicare_tax": {},
      "medicare_wages": {},
      "meta": {},
      "non_qualified_plans": {},
      "pdf_url": "https://example.com",
      "ss_tax": {},
      "ss_tips": {},
      "ss_wages": {},
      "states": [
        {}
      ],
      "updated_date": "string",
      "wages_other_comps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advance_eic_payment` | object |  |
| `allocated_tips` | object |  |
| `control_number` | object |  |
| `created_date` | string |  |
| `dependent_care_benefits` | object |  |
| `ein` | object |  |
| `employee_address` | object |  |
| `employee_name` | object |  |
| `employee_ssn` | object |  |
| `employer_address` | object |  |
| `employer_name` | object |  |
| `external_id` | string |  |
| `federal_income_tax` | object |  |
| `field_12a_col1` | object |  |
| `field_12a_col2` | object |  |
| `field_12b_col1` | object |  |
| `field_12b_col2` | object |  |
| `field_12c_col1` | object |  |
| `field_12c_col2` | object |  |
| `field_12d_col1` | object |  |
| `field_12d_col2` | object |  |
| `field_14_other` | array<object> |  |
| `id` | number |  |
| `img_thumbnail_url` | string |  |
| `is_13a` | object |  |
| `is_13b` | object |  |
| `is_13c` | object |  |
| `medicare_tax` | object |  |
| `medicare_wages` | object |  |
| `meta` | object |  |
| `non_qualified_plans` | object |  |
| `pdf_url` | string |  |
| `ss_tax` | object |  |
| `ss_tips` | object |  |
| `ss_wages` | object |  |
| `states` | array<object> |  |
| `updated_date` | string |  |
| `wages_other_comps` | object |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/w2s/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-w2s-document-id.md) for the provider-specific parameters and requirements.

