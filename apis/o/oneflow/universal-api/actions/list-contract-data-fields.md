# Oneflow: List Contract Data Fields

Retrieves contract data fields from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contract-data-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contract-data-fields?connectionId=$CONNECTION_ID&limit=25&offset=0&contractId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contractId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-contract-data-fields?${params}`, {
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
| `contractId` | string | yes | The Oneflow contract ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "custom_id": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "placeholder": "string",
      "source": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `custom_id` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `placeholder` | string |  |
| `source` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `GET /contracts/:contractId/data_fields` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contract-data-fields.md) for the provider-specific parameters and requirements.

