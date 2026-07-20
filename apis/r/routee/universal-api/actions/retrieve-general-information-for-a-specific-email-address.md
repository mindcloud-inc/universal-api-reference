# Routee: Retrieve general information for a specific email address

Retrieves general information for a specific email address from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-general-information-for-a-specific-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-general-information-for-a-specific-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-general-information-for-a-specific-email-address?${params}`, {
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
| `email` | string | yes | The email to retrieve information |

## Response

```json
{
  "success": true,
  "data": [
    {
      "book_id": "string",
      "email": "ava@example.com",
      "status": "string",
      "variables": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `book_id` | string |  |
| `email` | string |  |
| `status` | string |  |
| `variables[]` | array<object> |  |
| `variables[].name` | string |  |
| `variables[].type` | string |  |
| `variables[].value` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /emails/:email` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-general-information-for-a-specific-email-address.md) for the provider-specific parameters and requirements.

