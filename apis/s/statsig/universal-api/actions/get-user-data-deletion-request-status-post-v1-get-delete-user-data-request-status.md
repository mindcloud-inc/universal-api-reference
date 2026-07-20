# Statsig: Get User Data Deletion Request Status

Retrieves a user data deletion request status from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-user-data-deletion-request-status-post-v1-get-delete-user-data-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-user-data-deletion-request-status-post-v1-get-delete-user-data-request-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-user-data-deletion-request-status-post-v1-get-delete-user-data-request-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Deletion request ID returned by Create User Data Deletion Request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Deletion status: COMPLETE, PENDING, or UNKNOWN. |

## Native endpoint

Through the native Statsig API, this operation is `POST /v1/get_delete_user_data_request_status` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-data-deletion-request-status-post-v1-get-delete-user-data-request-status.md) for the provider-specific parameters and requirements.

