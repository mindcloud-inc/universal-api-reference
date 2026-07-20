# Paycove: Get Application Status

Retrieves a gateway application status from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-application-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-application-status?connectionId=$CONNECTION_ID&uniqueAccountId=c992329175ebd88509430024bcaba5da" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueAccountId": "c992329175ebd88509430024bcaba5da"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-application-status?${params}`, {
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
| `uniqueAccountId` | string | yes | Paycove account unique_id. Example: `c992329175ebd88509430024bcaba5da`. |

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
| `status` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `GET https://paycove.io/gateway-application-status/:unique_account_id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application-status.md) for the provider-specific parameters and requirements.

