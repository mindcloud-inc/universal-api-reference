# turboSMTP: Validate Email

Validates an email address in turboSMTP.

```
POST https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/validate-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/validate-email', {
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
      "account": "string",
      "city": "string",
      "country": "string",
      "did_you_mean": "string",
      "domain": "string",
      "domain_age_days": 1,
      "email": "ava@example.com",
      "firstname": "Ava",
      "free_email": true,
      "gender": "string",
      "lastname": "Chen",
      "mx_found": true,
      "mx_record": "string",
      "processed_at": "string",
      "region": "string",
      "smtp_provider": "string",
      "status": "string",
      "sub_status": "string",
      "zipcode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `city` | string |  |
| `country` | string |  |
| `did_you_mean` | string |  |
| `domain` | string |  |
| `domain_age_days` | number |  |
| `email` | string |  |
| `firstname` | string |  |
| `free_email` | boolean |  |
| `gender` | string |  |
| `lastname` | string |  |
| `mx_found` | boolean |  |
| `mx_record` | string |  |
| `processed_at` | string |  |
| `region` | string |  |
| `smtp_provider` | string |  |
| `status` | string |  |
| `sub_status` | string |  |
| `zipcode` | number |  |

## Native endpoint

Through the native turboSMTP API, this operation is `POST /emailvalidation/validateEmail` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

