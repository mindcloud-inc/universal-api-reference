# Thinkific: Update Enrollment

Updates an existing enrollment in Thinkific.

```
PUT https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/update-enrollment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/update-enrollment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/update-enrollment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activatedAt` | date | no | Updated activation timestamp. |
| `expiryDate` | date | no | Updated expiry date. |
| `id` | number | yes | Enrollment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the enrollment is updated successfully. |

## Native endpoint

Through the native Thinkific API, this operation is `PUT /enrollments/:id` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-enrollment.md) for the provider-specific parameters and requirements.

