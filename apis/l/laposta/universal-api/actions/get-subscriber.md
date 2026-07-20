# Laposta: Get Subscriber

Retrieves a subscriber from Laposta.

```
GET https://connect.mindcloud.co/v1/universal/laposta/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&memberId=string&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memberId": "string",
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laposta/latest/actions/get-subscriber?${params}`, {
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
| `memberId` | string | yes | The subscriber ID or email address to retrieve. |
| `listId` | string | yes | The ID of the list that owns the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "member": {
        "email": "ava@example.com",
        "listId": "string",
        "memberId": "string",
        "signupDate": "string",
        "sourceUrl": "https://example.com",
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `member` | object |  |
| `member.email` | string |  |
| `member.listId` | string |  |
| `member.memberId` | string |  |
| `member.signupDate` | string |  |
| `member.sourceUrl` | string |  |
| `member.state` | string |  |

## Native endpoint

Through the native Laposta API, this operation is `GET /member/:memberId` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

