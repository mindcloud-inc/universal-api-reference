# Wasabi: Create Bucket

Creates a new bucket in Wasabi.

```
POST https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/create-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/create-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "mindcloud-wasabi-agent-20260422"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/create-bucket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "mindcloud-wasabi-agent-20260422"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Globally unique DNS-compatible bucket name. Example: `mindcloud-wasabi-agent-20260422`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location` | string | Provider location path for the created bucket. |
| `name` | string | Created bucket name. |

## Native endpoint

Through the native Wasabi API, this operation is `PUT /:name` (base URL `https://s3.wasabisys.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bucket.md) for the provider-specific parameters and requirements.

