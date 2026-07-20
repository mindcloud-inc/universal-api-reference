# White Swan: Add Case Party

Adds a case party to a White Swan case.

```
POST https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/add-case-party
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/add-case-party" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/add-case-party', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | string | yes | White Swan request ID to grant access to. |
| `inviteeEmail` | string | no | Email that should receive case access. |
| `inviteePhone` | string | no | Phone number that should receive case access. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error_message": "string",
      "request": "string",
      "request_parties": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error_message` | string |  |
| `request` | string |  |
| `request_parties` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native White Swan API, this operation is `POST /invite_case_party` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-case-party.md) for the provider-specific parameters and requirements.

