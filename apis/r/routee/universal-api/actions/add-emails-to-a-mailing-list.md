# Routee: Add emails to a mailing list

Adds emails to a mailing list in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-emails-to-a-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-emails-to-a-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-emails-to-a-mailing-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | List ID |
| `emails[]` | array<string> | no | A serialized array of emails |
| `email` | string | no | The email to be added to the mailing list |
| `variables` | string | no | The variables to add to the email |
| `phone` | string | no | To add a phone number, use the system variable Phone |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |

## Native endpoint

Through the native Routee API, this operation is `POST /addressbooks/:id/emails` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-emails-to-a-mailing-list.md) for the provider-specific parameters and requirements.

