# LinkedCamp: Get Account API Token



```
GET https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-account-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-account-api-token?connectionId=$CONNECTION_ID&accountEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-account-api-token?${params}`, {
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
| `accountEmail` | string | yes | Account email to retrieve an API token for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | LinkedCamp status message. |
| `success` | boolean | Whether the operation succeeded. |
| `token` | string | API token for the requested account. |

## Native endpoint

Through the native LinkedCamp API, this operation is `GET /tokens` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-api-token.md) for the provider-specific parameters and requirements.

