# Routee: Retrieve information for specific email address from a mailing list

Retrieves information for specific email address from a mailing list in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-information-for-specific-email-address-from-a-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-information-for-specific-email-address-from-a-mailing-list?connectionId=$CONNECTION_ID&id=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-information-for-specific-email-address-from-a-mailing-list?${params}`, {
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
| `id` | string | yes | List ID |
| `email` | string | yes | Email address information is desired on |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abook_id": "string",
      "email": "ava@example.com",
      "status": "string",
      "status_explain": "string",
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
| `abook_id` | string |  |
| `email` | string |  |
| `status` | string |  |
| `status_explain` | string |  |
| `variables[]` | array<object> |  |
| `variables[].name` | string |  |
| `variables[].type` | string |  |
| `variables[].value` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /addressbooks/:id/emails/:email` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-information-for-specific-email-address-from-a-mailing-list.md) for the provider-specific parameters and requirements.

