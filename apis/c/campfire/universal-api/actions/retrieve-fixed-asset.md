# Campfire: Retrieve Fixed Asset

Retrieves a fixed asset from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-fixed-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-fixed-asset?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-fixed-asset?${params}`, {
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
| `id` | number | yes | The fixed asset ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accumulated_depreciation_account_name": "Ava Chen",
      "asset_account_name": "Ava Chen",
      "asset_class": 1,
      "asset_class_name": "Ava Chen",
      "attachments": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "department": 1,
      "department_name": "Ava Chen",
      "depreciation_end_date": "2026-05-07T12:00:00.000Z",
      "depreciation_expense_account_name": "Ava Chen",
      "depreciation_start_date": "2026-05-07T12:00:00.000Z",
      "depreciations": [
        {}
      ],
      "disposals": [
        {}
      ],
      "entity": 1,
      "entity_currency": "string",
      "entity_name": "Ava Chen",
      "exchange_rate": 1,
      "id": 1,
      "initial_value": 1,
      "is_deleted": true,
      "is_non_depreciable": true,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "net_book_value": "string",
      "purchase_date": "2026-05-07T12:00:00.000Z",
      "salvage_value": 1,
      "status": "string",
      "tags": [
        {}
      ],
      "useful_life": "string",
      "vendor": 1,
      "vendor_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accumulated_depreciation_account_name` | string |  |
| `asset_account_name` | string |  |
| `asset_class` | number |  |
| `asset_class_name` | string |  |
| `attachments` | array<object> |  |
| `created_at` | date |  |
| `currency` | string |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `department` | number |  |
| `department_name` | string |  |
| `depreciation_end_date` | date |  |
| `depreciation_expense_account_name` | string |  |
| `depreciation_start_date` | date |  |
| `depreciations` | array<object> |  |
| `disposals` | array<object> |  |
| `entity` | number |  |
| `entity_currency` | string |  |
| `entity_name` | string |  |
| `exchange_rate` | number |  |
| `id` | number |  |
| `initial_value` | number |  |
| `is_deleted` | boolean |  |
| `is_non_depreciable` | boolean |  |
| `last_modified_at` | date |  |
| `name` | string |  |
| `net_book_value` | string |  |
| `purchase_date` | date |  |
| `salvage_value` | number |  |
| `status` | string |  |
| `tags` | array<object> |  |
| `useful_life` | string |  |
| `vendor` | number |  |
| `vendor_name` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/fixed-asset/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-fixed-asset.md) for the provider-specific parameters and requirements.

