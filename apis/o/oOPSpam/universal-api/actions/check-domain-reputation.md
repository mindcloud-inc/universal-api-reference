# OOPSpam: Check Domain Reputation

Checks a domain's reputation in OOPSpam.

```
GET https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-domain-reputation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OOPSpam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-domain-reputation?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-domain-reputation?${params}`, {
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
| `domain` | string | yes | Fully qualified domain name without protocol or www. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "blocker": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `blocker[]` | string |  |

## Native endpoint

Through the native OOPSpam API, this operation is `POST /reputation/domain` (base URL `https://api.oopspam.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain-reputation.md) for the provider-specific parameters and requirements.

