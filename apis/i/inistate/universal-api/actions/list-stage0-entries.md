# Inistate: List Stage0 Entries

Retrieves Stage0 entries from Inistate.

```
GET https://connect.mindcloud.co/v1/universal/inistate/latest/actions/list-stage0-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inistate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inistate/latest/actions/list-stage0-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inistate/latest/actions/list-stage0-entries?${params}`, {
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
| `currentPage` | number | no | Zero-based page number. Default: `0`. |
| `pageSize` | number | no | Number of entries to return per page. Use 0 only if you intentionally want the provider's all-rows behavior. Default: `20`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | no | Optional QueryFilterProcessor payload. Use the provider's documented `filters.items` structure; sorting is intentionally omitted because live provider runs currently fail when `sorts` is supplied. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Page envelope containing `pageSize`, `currentPage`, `list`, `totalItems`, and `limit`. |

## Native endpoint

Through the native Inistate API, this operation is `POST /api/workspace/list` (base URL `https://api.inistate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stage0-entries.md) for the provider-specific parameters and requirements.

