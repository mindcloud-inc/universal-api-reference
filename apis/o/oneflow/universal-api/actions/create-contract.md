# Oneflow: Create Contract

Creates a contract in Oneflow.

```
POST https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "templateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "templateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes | The Oneflow workspace ID where the contract will be created. |
| `templateId` | number | yes | The Oneflow template ID to use when creating the contract. |

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
      "sign_order": [
        {}
      ],
      "signing_period_expiry_time": "string",
      "state": "string",
      "state_updated_time": "string",
      "tags": [
        {}
      ],
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `_permissions` | object |  |
| `_private` | object |  |
| `_private_ownerside` | object |  |
| `attachment_file_groups` | array<object> |  |
| `available_options` | object |  |
| `data_fields` | array<object> |  |
| `id` | number |  |
| `lifecycle_settings` | object |  |
| `lifecycle_state` | object |  |
| `parties` | array<object> |  |
| `pdf_file_groups` | array<object> |  |
| `product_groups` | array<object> |  |
| `published_time` | string |  |
| `sign_order` | array<object> |  |
| `signing_period_expiry_time` | string |  |
| `state` | string |  |
| `state_updated_time` | string |  |
| `tags` | array<object> |  |
| `updated_time` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `POST /contracts/create` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract.md) for the provider-specific parameters and requirements.

