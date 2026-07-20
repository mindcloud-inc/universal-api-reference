# SendPulse: Update Mailing List

Updates an existing mailing list in SendPulse.

```
PUT https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "123456",
  "name": "Updated Newsletter Subscribers"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-mailing-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "123456",
    "name": "Updated Newsletter Subscribers"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailingListId` | string | yes | The SendPulse mailing list identifier. Example: `123456`. |
| `name` | string | yes | Updated name for the mailing list. Example: `Updated Newsletter Subscribers`. |

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

Through the native SendPulse API, this operation is `PUT /addressbooks/:mailingListId` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mailing-list.md) for the provider-specific parameters and requirements.

