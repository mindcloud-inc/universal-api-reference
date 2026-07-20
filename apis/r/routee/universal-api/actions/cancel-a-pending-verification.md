# Routee: Cancel a pending verification

Cancels a pending verification in Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/cancel-a-pending-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/cancel-a-pending-verification?connectionId=$CONNECTION_ID&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/cancel-a-pending-verification?${params}`, {
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
| `trackingId` | string | yes | the tracking id of the verification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "string",
      "maxRetries": 1,
      "status": "string",
      "timesTried": 1,
      "trackingId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | string |  |
| `maxRetries` | number |  |
| `status` | string |  |
| `timesTried` | number |  |
| `trackingId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Routee API, this operation is `DELETE /2step/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-a-pending-verification.md) for the provider-specific parameters and requirements.

