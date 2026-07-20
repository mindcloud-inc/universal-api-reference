# Selzy: Get Contact

Retrieves a contact from Selzy.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-contact?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/get-contact?${params}`, {
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
| `email` | string | yes | Email address of the contact to retrieve. |
| `includeLists` | number | no | Set to 1 to include contact list memberships. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeFields` | number | no | Set to 1 to include custom contact fields. |
| `includeDetails` | number | no | Set to 1 to include detailed activity metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "email": {
          "added_at": "2026-05-07T12:00:00.000Z",
          "availability": "ava@example.com",
          "email": "ava@example.com",
          "status": "ava@example.com"
        },
        "lists": [
          {
            "added_at": "2026-05-07T12:00:00.000Z",
            "id": 1,
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
| `result.email.added_at` | date |  |
| `result.email.availability` | string |  |
| `result.email.email` | string |  |
| `result.email.status` | string |  |
| `result.lists[].added_at` | date |  |
| `result.lists[].id` | number |  |
| `result.lists[].status` | string |  |

## Native endpoint

Through the native Selzy API, this operation is `POST getContact` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

