# Ortto: Subscribe Audience Members



```
PUT https://connect.mindcloud.co/v1/universal/ortto/latest/actions/subscribe-audience-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/subscribe-audience-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audienceId": "string",
  "people[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/subscribe-audience-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audienceId": "string",
    "people[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audienceId` | string | yes | Audience to subscribe people to. |
| `people[]` | array<object> | yes | Audience member updates. |
| `async` | boolean | no | Queue the subscription update asynchronously. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audienceId": "string",
      "people": [
        {
          "personStatus": "string",
          "status": "string"
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
| `audienceId` | string |  |
| `people[].personStatus` | string |  |
| `people[].status` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `PUT /audience/subscribe` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-audience-members.md) for the provider-specific parameters and requirements.

