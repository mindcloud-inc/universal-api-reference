# TouchBasePro: Get Validation List Status

Retrieves validation list status from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-validation-list-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-validation-list-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-validation-list-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "errorMessage": "string",
      "isSuccessful": true,
      "name": "Ava Chen",
      "requestId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `duration` | number |  |
| `errorMessage` | string |  |
| `isSuccessful` | boolean |  |
| `name` | string |  |
| `requestId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /validate/GetListValidationStatus?RequestId={RequestId}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-list-status.md) for the provider-specific parameters and requirements.

