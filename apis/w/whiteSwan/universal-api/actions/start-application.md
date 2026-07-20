# White Swan: Start Application

Starts an application for a White Swan personal plan.

```
POST https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/start-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/start-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "plan": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/start-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "plan": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `plan` | string | yes | White Swan personal plan ID to start an application for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error_message` | string |  |

## Native endpoint

Through the native White Swan API, this operation is `POST /start_application` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-application.md) for the provider-specific parameters and requirements.

