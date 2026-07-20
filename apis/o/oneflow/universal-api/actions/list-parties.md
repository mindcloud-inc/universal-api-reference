# Oneflow: List Parties

Retrieves contract parties from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-parties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-parties?connectionId=$CONNECTION_ID&limit=25&offset=0&contractId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contractId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-parties?${params}`, {
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
      "country_code": "string",
      "id": 1,
      "identification_number": "string",
      "my_party": true,
      "name": "Ava Chen",
      "participants": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string |  |
| `id` | number |  |
| `identification_number` | string |  |
| `my_party` | boolean |  |
| `name` | string |  |
| `participants` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `GET /contracts/:contractId/parties` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-parties.md) for the provider-specific parameters and requirements.

