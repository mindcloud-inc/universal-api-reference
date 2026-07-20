# Oneflow: Publish Contract

Publishes a contract in Oneflow.

```
PUT https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/publish-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/publish-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "subject": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/publish-contract', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "subject": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Oneflow contract ID. |
| `subject` | string | yes | The invitation email subject sent when the contract is published. |
| `message` | string | yes | The invitation message sent when the contract is published. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "published_time": "string",
      "state": "string",
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `published_time` | string |  |
| `state` | string |  |
| `updated_time` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `POST /contracts/:id/publish` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-contract.md) for the provider-specific parameters and requirements.

