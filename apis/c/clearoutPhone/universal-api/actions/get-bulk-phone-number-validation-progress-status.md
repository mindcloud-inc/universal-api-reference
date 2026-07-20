# ClearoutPhone: Get Bulk Phone Number Validation Progress Status

Retrieves the progress status of a bulk validation job in ClearoutPhone.

```
GET https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-bulk-phone-number-validation-progress-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearoutPhone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-bulk-phone-number-validation-progress-status?connectionId=$CONNECTION_ID&listId=5cc81d0589c374444f03a5a4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "5cc81d0589c374444f03a5a4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-bulk-phone-number-validation-progress-status?${params}`, {
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
| `listId` | string | yes | Bulk validation list identifier Example: `5cc81d0589c374444f03a5a4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "percentile": 1,
      "progressStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `percentile` | number |  |
| `progressStatus` | string |  |

## Native endpoint

Through the native ClearoutPhone API, this operation is `GET /phonenumber/bulk/progress_status` (base URL `https://api.clearoutphone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-phone-number-validation-progress-status.md) for the provider-specific parameters and requirements.

