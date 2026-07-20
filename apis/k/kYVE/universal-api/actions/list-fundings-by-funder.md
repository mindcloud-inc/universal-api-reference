# KYVE: List Fundings By Funder



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-fundings-by-funder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-fundings-by-funder?connectionId=$CONNECTION_ID&limit=25&offset=0&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-fundings-by-funder?${params}`, {
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
| `address` | string | yes | KYVE funder address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fundings": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fundings` | array<object> |  |
| `pagination` | object |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/query/v1beta1/fundings_by_funder/{address}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fundings-by-funder.md) for the provider-specific parameters and requirements.

