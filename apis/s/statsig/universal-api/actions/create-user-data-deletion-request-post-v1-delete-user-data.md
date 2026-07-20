# Statsig: Create User Data Deletion Request

Creates a user data deletion request in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-user-data-deletion-request-post-v1-delete-user-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-user-data-deletion-request-post-v1-delete-user-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "unitType": "user_id",
  "ids": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-user-data-deletion-request-post-v1-delete-user-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "unitType": "user_id",
    "ids": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unitType` | string | yes | Unit type for deletion. Statsig currently supports user_id. Default: `user_id`. |
| `ids` | string | yes | Delimited list of IDs to delete data for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `delimiter` | string | no | Optional delimiter when IDs contain commas. |
| `requestId` | string | no | Optional unique request ID to track the deletion request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request_id` | string | Deletion request ID. |

## Native endpoint

Through the native Statsig API, this operation is `POST /v1/delete_user_data` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-data-deletion-request-post-v1-delete-user-data.md) for the provider-specific parameters and requirements.

