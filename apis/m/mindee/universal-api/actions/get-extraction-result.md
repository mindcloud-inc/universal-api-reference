# Mindee: Get Extraction Result

Retrieves an extraction result from Mindee.

```
GET https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-extraction-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mindee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-extraction-result?connectionId=$CONNECTION_ID&inferenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-extraction-result?${params}`, {
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
| `inferenceId` | string | yes | UUID of the inference to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inference": {
        "active_options": {
          "confidence": true,
          "data_schema": {
            "replace": true
          },
          "multipage_context": true,
          "polygon": true,
          "rag": true,
          "raw_text": true,
          "text_context": true
        },
        "file": {
          "mime_type": "string",
          "name": "Ava Chen",
          "page_count": 1
        },
        "id": "string",
        "job": {
          "id": "string"
        },
        "model": {
          "id": "string"
        },
        "result": {
          "fields": {
            "date": {
              "value": "2026-05-07T12:00:00.000Z"
            },
            "document_type": {
              "value": "string"
            },
            "line_items": {
              "items": [
                {
                  "fields": {
                    "description": {
                      "value": "string"
                    },
                    "quantity": {
                      "value": 1
                    },
                    "total_price": {
                      "value": 1
                    },
                    "unit_price": {
                      "value": 1
                    }
                  }
                }
              ]
            },
            "locale": {
              "fields": {
                "country": {
                  "value": "string"
                },
                "language": {
                  "value": "string"
                }
              }
            },
            "purchase_category": {
              "value": "string"
            },
            "purchase_subcategory": {
              "value": "string"
            },
            "receipt_number": {
              "value": "string"
            },
            "supplier_address": {
              "value": "string"
            },
            "supplier_company_registration": {
              "items": [
                {
                  "fields": {
                    "number": {
                      "value": "string"
                    },
                    "type": {
                      "value": "string"
                    }
                  }
                }
              ]
            },
            "supplier_name": {
              "value": "Ava Chen"
            },
            "supplier_phone_number": {
              "value": "string"
            },
            "time": {
              "value": "string"
            },
            "total_amount": {
              "value": 1
            },
            "total_tax": {
              "value": 1
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inference.active_options.confidence` | boolean |  |
| `inference.active_options.data_schema.replace` | boolean |  |
| `inference.active_options.multipage_context` | boolean |  |
| `inference.active_options.polygon` | boolean |  |
| `inference.active_options.rag` | boolean |  |
| `inference.active_options.raw_text` | boolean |  |
| `inference.active_options.text_context` | boolean |  |
| `inference.file.mime_type` | string |  |
| `inference.file.name` | string |  |
| `inference.file.page_count` | number |  |
| `inference.id` | string |  |
| `inference.job.id` | string |  |
| `inference.model.id` | string |  |
| `inference.result.fields.date.value` | date |  |
| `inference.result.fields.document_type.value` | string |  |
| `inference.result.fields.line_items.items[].fields.description.value` | string |  |
| `inference.result.fields.line_items.items[].fields.quantity.value` | number |  |
| `inference.result.fields.line_items.items[].fields.total_price.value` | number |  |
| `inference.result.fields.line_items.items[].fields.unit_price.value` | number |  |
| `inference.result.fields.locale.fields.country.value` | string |  |
| `inference.result.fields.locale.fields.language.value` | string |  |
| `inference.result.fields.purchase_category.value` | string |  |
| `inference.result.fields.purchase_subcategory.value` | string |  |
| `inference.result.fields.receipt_number.value` | string |  |
| `inference.result.fields.supplier_address.value` | string |  |
| `inference.result.fields.supplier_company_registration.items[].fields.number.value` | string |  |
| `inference.result.fields.supplier_company_registration.items[].fields.type.value` | string |  |
| `inference.result.fields.supplier_name.value` | string |  |
| `inference.result.fields.supplier_phone_number.value` | string |  |
| `inference.result.fields.time.value` | string |  |
| `inference.result.fields.total_amount.value` | number |  |
| `inference.result.fields.total_tax.value` | number |  |

## Native endpoint

Through the native Mindee API, this operation is `GET /v2/products/extraction/results/:inference_id` (base URL `https://api-v2.mindee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extraction-result.md) for the provider-specific parameters and requirements.

