# CircleCI: Create Checkout Key



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-checkout-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-checkout-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-checkout-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectSlug` | string | no | Project slug in the form vcs/org/repo. |
| `type` | string | no | Checkout key type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fingerprint": "string",
      "preferred": true,
      "publicKey": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fingerprint` | string |  |
| `preferred` | boolean |  |
| `publicKey` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /project/:project_slug/checkout-key` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout-key.md) for the provider-specific parameters and requirements.

