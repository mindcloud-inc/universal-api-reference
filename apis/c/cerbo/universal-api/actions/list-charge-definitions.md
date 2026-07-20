# Cerbo: List Charge Definitions

Retrieves charge definitions from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-charge-definitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-charge-definitions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-charge-definitions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Cerbo API, this operation is `GET /charge_master` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-charge-definitions.md) for the provider-specific parameters and requirements.

