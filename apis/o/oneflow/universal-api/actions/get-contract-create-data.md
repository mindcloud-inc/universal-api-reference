# Oneflow: Get Contract Create Data

Retrieves contract creation data from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contract-create-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contract-create-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contract-create-data?${params}`, {
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
| `extensionType` | string | no | Filter contract creation data by integration extension type. |
| `templateTypeId` | number | no | Filter contract creation data by template type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "templates": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `templates[].id` | number |  |
| `templates[].name` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `GET /helpers/contract_create_data` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contract-create-data.md) for the provider-specific parameters and requirements.

