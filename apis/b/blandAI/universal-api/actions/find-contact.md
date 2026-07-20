# Bland AI: Find Contact

Finds a contact in Bland AI.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/find-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/find-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/find-contact?${params}`, {
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
| `phoneNumber` | string | no |  |
| `email` | string | no |  |
| `externalId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "errors": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `errors` | array<object> |  |

## Native endpoint

Through the native Bland AI API, this operation is `POST /v1/contacts/find` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contact.md) for the provider-specific parameters and requirements.

