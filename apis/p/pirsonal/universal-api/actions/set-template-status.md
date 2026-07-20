# Pirsonal: Set Template Status

Updates the status of an existing template in Pirsonal.

```
PUT https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/set-template-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/set-template-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateID": "string",
  "status": "active"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/set-template-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateID": "string",
    "status": "active"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateID` | string | yes | ID of the template whose status should change. |
| `status` | list<string> | yes | Template status: active or inactive. One of: `active`, `inactive`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Pirsonal status-change response, normally OK. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-template-status.md) for the provider-specific parameters and requirements.

