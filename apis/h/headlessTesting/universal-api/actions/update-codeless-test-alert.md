# Headless Testing: Update Codeless Test Alert

Updates a codeless test alert in Headless Testing.

```
PUT https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-codeless-test-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-codeless-test-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "id": "string",
  "kind": "string",
  "level": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-codeless-test-alert', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "id": "string",
    "kind": "string",
    "level": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Alert target email, phone number, or callback URL. |
| `id` | string | yes | The codeless test identifier. |
| `kind` | string | yes | Alert delivery kind. |
| `level` | string | yes | Alert frequency level. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "kind": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `kind` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Headless Testing API, this operation is `PUT /lab/:id/alert` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-codeless-test-alert.md) for the provider-specific parameters and requirements.

