# Qive: List NFe Manifests V2



```
GET https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-nfe-manifests-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-nfe-manifests-v2?connectionId=$CONNECTION_ID&limit=25&offset=0&accessKeys%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accessKeys[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-nfe-manifests-v2?${params}`, {
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
| `accessKeys[]` | array<string> | yes | NFe access keys to retrieve manifest information for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_key": "string",
      "code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_key` | string |  |
| `code` | string |  |

## Native endpoint

Through the native Qive API, this operation is `GET /v2/nfe/manifest` (base URL `https://sandbox-api.arquivei.com.br`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfe-manifests-v2.md) for the provider-specific parameters and requirements.

