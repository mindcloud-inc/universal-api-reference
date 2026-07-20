# CircleCI: Create Context



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-context" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Context",
  "owner": {
    "id": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16",
    "type": "organization"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-context', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Context",
    "owner": {"id":"afbcafd1-31ea-4324-bc26-bf5d7e8e3e16","type":"organization"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The context name. Default: `MindCloud Context`. |
| `owner` | object | yes | Context owner object with organization id or slug and type. Default: `{"id":"afbcafd1-31ea-4324-bc26-bf5d7e8e3e16","type":"organization"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /context` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-context.md) for the provider-specific parameters and requirements.

