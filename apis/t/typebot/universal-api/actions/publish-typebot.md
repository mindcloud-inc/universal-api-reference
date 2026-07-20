# Typebot: Publish Typebot



```
PUT https://connect.mindcloud.co/v1/universal/typebot/latest/actions/publish-typebot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/publish-typebot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "typebotId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typebot/latest/actions/publish-typebot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "typebotId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `typebotId` | string | yes | The Typebot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "warnings": [
        {
          "trademark": "string",
          "type": "string"
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
| `message` | string |  |
| `warnings[].trademark` | string |  |
| `warnings[].type` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `POST /v1/typebots/:typebotId/publish` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-typebot.md) for the provider-specific parameters and requirements.

