# WotNot: List Bots

Retrieves bots from WotNot.

```
GET https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/list-bots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/list-bots?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/list-bots?${params}`, {
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
| `accountId` | number | yes | WotNot account or workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bots": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bots` | array<object> | Bots available in the account. |
| `ok` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native WotNot API, this operation is `GET /v1/accounts/:account_id/bots` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bots.md) for the provider-specific parameters and requirements.

