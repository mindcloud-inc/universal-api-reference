# Selzy: Get Total Contact Count

Retrieves the total contact count for a Selzy user.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-total-contact-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-total-contact-count?connectionId=$CONNECTION_ID&login=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "login": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-total-contact-count?${params}`, {
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
| `login` | string | yes | Selzy user login, as shown in the Selzy account, not necessarily the email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.total` | number |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getTotalContactsCount` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-contact-count.md) for the provider-specific parameters and requirements.

