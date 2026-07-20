# Selzy: Check Email

Retrieves the delivery status of a Selzy email.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/check-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/check-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/check-email?${params}`, {
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
      "failed_email_id": [
        {}
      ],
      "result": {
        "statuses": [
          {
            "id": "string",
            "status": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed_email_id` | array<object> |  |
| `result.statuses[].id` | string |  |
| `result.statuses[].status` | string |  |

## Native endpoint

Through the native Selzy API, this operation is `POST checkEmail` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-email.md) for the provider-specific parameters and requirements.

