# Laposta: List Subscribers

Retrieves subscribers from Laposta.

```
GET https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-subscribers?${params}`, {
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
| `listId` | string | yes | The ID of the list whose subscribers to list. |
| `state` | list | no | Optional subscriber state selector. One of: `active`, `cleaned`, `unsubscribed`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "member": {
            "email": "ava@example.com",
            "memberId": "string",
            "signupDate": "string",
            "state": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].member` | object |  |
| `data[].member.email` | string |  |
| `data[].member.memberId` | string |  |
| `data[].member.signupDate` | string |  |
| `data[].member.state` | string |  |

## Native endpoint

Through the native Laposta API, this operation is `GET /member` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

