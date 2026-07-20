# fal.ai: Create Compute Instance

Creates a compute instance in fal.ai.

```
POST https://connect.mindcloud.co/v1/universal/falai/latest/actions/create-compute-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/falai/latest/actions/create-compute-instance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instanceType": "string",
  "sshKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/falai/latest/actions/create-compute-instance', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instanceType": "string",
    "sshKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instanceType` | string | yes | Compute instance type to create. |
| `sshKey` | string | yes | SSH public key that will be installed on the new instance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator_user_nickname": "Ava Chen",
      "id": "string",
      "instance_type": "string",
      "ip": "string",
      "region": "string",
      "sector": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator_user_nickname` | string |  |
| `id` | string |  |
| `instance_type` | string |  |
| `ip` | string |  |
| `region` | string |  |
| `sector` | string |  |
| `status` | string |  |

## Native endpoint

Through the native fal.ai API, this operation is `POST /compute/instances` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-compute-instance.md) for the provider-specific parameters and requirements.

