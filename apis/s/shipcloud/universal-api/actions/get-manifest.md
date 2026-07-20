# Shipcloud: Get Manifest

Retrieves a manifest from Shipcloud by ID.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-manifest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-manifest?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-manifest?${params}`, {
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
| `id` | string | yes | The Shipcloud manifest identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrier_reference_number": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "documents": [
        {}
      ],
      "id": "string",
      "posting_hub_address": {},
      "reference_number": "string",
      "shipments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrier_reference_number` | string |  |
| `created_at` | date |  |
| `documents` | array<object> |  |
| `id` | string |  |
| `posting_hub_address` | object |  |
| `reference_number` | string |  |
| `shipments` | array<object> |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /manifests/:id` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-manifest.md) for the provider-specific parameters and requirements.

