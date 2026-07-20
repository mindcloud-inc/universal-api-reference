# HR Partner: Add or Update Applicant



```
PUT https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-applicant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-applicant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-applicant', {
  method: 'PUT',
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
      "email": "ava@example.com",
      "firstNames": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "jobApplications": [
        {}
      ],
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstNames` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `jobApplications` | array<object> |  |
| `lastName` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `POST /applicant` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-update-applicant.md) for the provider-specific parameters and requirements.

