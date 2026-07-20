# SendPulse: Create Mailing List

Creates a new mailing list in SendPulse.

```
POST https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookName": "Newsletter Subscribers"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-mailing-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookName": "Newsletter Subscribers"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookName` | string | yes | Name of the new mailing list. Example: `Newsletter Subscribers`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native SendPulse API, this operation is `POST /addressbooks` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailing-list.md) for the provider-specific parameters and requirements.

