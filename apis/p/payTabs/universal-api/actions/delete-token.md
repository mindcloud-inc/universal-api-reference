# PayTabs: Delete Token



```
DELETE https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/delete-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/delete-token?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/delete-token?${params}`, {
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
| `token` | string | yes | Stored PayTabs token to revoke. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "deleted": true,
      "message": "string",
      "token": "string",
      "trace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `deleted` | boolean |  |
| `message` | string |  |
| `token` | string |  |
| `trace` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/token/delete` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-token.md) for the provider-specific parameters and requirements.

