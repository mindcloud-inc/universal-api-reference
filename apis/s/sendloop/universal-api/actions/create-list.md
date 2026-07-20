# Sendloop: Create List



```
POST https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "optInMode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "optInMode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the new list |
| `optInMode` | string | yes | Pass Single or Double |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listID": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listID` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /list.create/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

