# Tellephant: List unsubscribed contacts

Retrieves contacts by subscription status from Tellephant.

```
GET https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-unsubscribed-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-unsubscribed-contacts?connectionId=$CONNECTION_ID&type=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "all"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-unsubscribed-contacts?${params}`, {
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
| `type` | list | yes | Contact list type: all, unsubscribed, or blocked. One of: `all`, `blocked`, `unsubscribed`. Default: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "error": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `error` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tellephant API, this operation is `POST /v1/user/unsubscribe` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unsubscribed-contacts.md) for the provider-specific parameters and requirements.

