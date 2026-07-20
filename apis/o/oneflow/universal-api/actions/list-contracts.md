# Oneflow: List Contracts

Retrieves contracts from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contracts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contracts?${params}`, {
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
      "_links": {},
      "_permissions": {},
      "_private": {},
      "_private_ownerside": {},
      "attachment_file_groups": [
        {}
      ],
      "available_options": {},
      "data_fields": [
        {}
      ],
      "id": 1,
      "lifecycle_settings": {},
      "lifecycle_state": {},
      "links": [
        {}
      ],
      "parties": [
        {}
      ],
      "pdf_file_groups": [
        {}
      ],
      "product_groups": [
        {}
      ],
      "published_time": "string",
      "signing_period_expiry_time": "string",
      "state": "string",
      "state_updated_time": "string",
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Links related to the contract. |
| `_permissions` | object | Permissions available on the contract. |
| `_private` | object | Private contract data visible to the current party. |
| `_private_ownerside` | object | Owner-side private contract data. |
| `attachment_file_groups` | array<object> | Attachment file groups on the contract. |
| `available_options` | object | Available capabilities and options for the contract. |
| `data_fields` | array<object> | Data fields on the contract. |
| `id` | number | The unique contract ID. |
| `lifecycle_settings` | object | Lifecycle settings for the contract. |
| `lifecycle_state` | object | The current lifecycle state details. |
| `links` | array<object> | Links to related contracts. |
| `parties` | array<object> | Parties on the contract. |
| `pdf_file_groups` | array<object> | PDF file groups on the contract. |
| `product_groups` | array<object> | Product groups on the contract. |
| `published_time` | string | When the contract was published. |
| `signing_period_expiry_time` | string | When the signing period expires. |
| `state` | string | The contract signing state. |
| `state_updated_time` | string | When the contract state was last updated. |
| `updated_time` | string | When the contract was last updated. |

## Native endpoint

Through the native Oneflow API, this operation is `GET /contracts` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contracts.md) for the provider-specific parameters and requirements.

