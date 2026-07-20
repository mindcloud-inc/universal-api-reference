# Routee: Template creation

Creates a new template in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/template-creation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/template-creation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/template-creation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The name of the template (the parameter is optional, if not specified, the name will be displayed as Template YYYY.mm.dd H:i:s) |
| `body` | string | yes | HTML version of the email, encoded in base64 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "real_id": 1,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `real_id` | number |  |
| `result` | boolean |  |

## Native endpoint

Through the native Routee API, this operation is `POST /template` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/template-creation.md) for the provider-specific parameters and requirements.

