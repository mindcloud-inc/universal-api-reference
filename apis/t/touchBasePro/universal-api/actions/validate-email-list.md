# TouchBasePro: Validate Email List

Validates an email list in TouchBasePro.

```
POST https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/validate-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/validate-email-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/validate-email-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "isSuccessful": true,
      "requestId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSuccessful` | boolean |  |
| `requestId` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `POST /validate/ValidateEmailList` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-list.md) for the provider-specific parameters and requirements.

