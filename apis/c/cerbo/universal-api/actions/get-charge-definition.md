# Cerbo: Get Charge Definition

Retrieves charge definition details from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-charge-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-charge-definition?connectionId=$CONNECTION_ID&charge_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "charge_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-charge-definition?${params}`, {
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
| `charge_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "add_to_insurance_claims": true,
      "addedby": "string",
      "barcode_upc": "string",
      "category": "string",
      "cpt_code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "inactive": true,
      "is_special": true,
      "is_supply": true,
      "is_taxable": true,
      "name": "Ava Chen",
      "name_for_pt_portal": "Ava Chen",
      "nicknames": [
        "Ava Chen"
      ],
      "object": "string",
      "retail": "string",
      "tax_rate": "string",
      "time_required": "string",
      "wholesale": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_to_insurance_claims` | boolean |  |
| `addedby` | string |  |
| `barcode_upc` | string |  |
| `category` | string |  |
| `cpt_code` | string |  |
| `created` | date |  |
| `description` | string |  |
| `id` | string |  |
| `inactive` | boolean |  |
| `is_special` | boolean |  |
| `is_supply` | boolean |  |
| `is_taxable` | boolean |  |
| `name` | string |  |
| `name_for_pt_portal` | string |  |
| `nicknames` | array<string> |  |
| `object` | string |  |
| `retail` | string |  |
| `tax_rate` | string |  |
| `time_required` | string |  |
| `wholesale` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /charge_master/:charge_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge-definition.md) for the provider-specific parameters and requirements.

