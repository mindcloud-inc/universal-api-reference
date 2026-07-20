# Damstra Forms: Create Draft Action

Creates a draft action in Damstra Forms.

```
POST https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/create-draft-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/create-draft-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/create-draft-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload[]` | array<object> | yes | Array of draft action payloads. Each item follows the Damstra create draft action request body shape. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `POST /actions` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-action.md) for the provider-specific parameters and requirements.

