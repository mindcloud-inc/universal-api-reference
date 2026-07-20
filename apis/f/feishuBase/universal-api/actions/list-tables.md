# Feishu Base: List Tables

Retrieves tables from a Feishu Base app.

```
GET https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Base `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/list-tables?connectionId=$CONNECTION_ID&appToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/list-tables?${params}`, {
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
| `appToken` | string | yes | Unique identifier of the Feishu Base app. |
| `pageToken` | string | no | Pagination token returned by the previous page. |
| `pageSize` | number | no | Maximum number of tables to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `msg` | string |  |

## Native endpoint

Through the native Feishu Base API, this operation is `GET /apps/:app_token/tables` (base URL `https://open.feishu.cn/open-apis/bitable/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

