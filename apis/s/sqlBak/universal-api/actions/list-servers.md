# SqlBak: List Servers

Retrieves servers from SqlBak.

```
GET https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/list-servers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SqlBak `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/list-servers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sqlBak/latest/actions/list-servers?${params}`, {
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
| `name` | string | no | Filter servers whose name contains this substring. |
| `appType` | list | no | Filter servers by installed SqlBak application type. One of: `sqlbak_linux`, `sqlbak_windows`. |
| `status` | list | no | Filter servers by current connection status. One of: `disconnected`, `offline`, `online`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_more": true,
      "list": [
        {}
      ],
      "page": 1,
      "page_size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean | Whether another page can be requested. |
| `list` | array<object> | Servers returned for the current page. |
| `page` | number | Current page number. |
| `page_size` | number | Requested page size. |
| `total` | number | Total matching records. |

## Native endpoint

Through the native SqlBak API, this operation is `GET /servers` (base URL `https://sqlbak.com/public-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-servers.md) for the provider-specific parameters and requirements.

