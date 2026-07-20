# VoilaNorbert: Get Contact

Retrieves a single contact from VoilaNorbert.

```
GET https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | The contact id to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "created": 1,
      "email": {},
      "id": 1,
      "lists": [
        {}
      ],
      "messages": [
        {}
      ],
      "name": "Ava Chen",
      "owner": {},
      "searching": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `created` | number |  |
| `email` | object |  |
| `id` | number |  |
| `lists` | array<object> |  |
| `messages` | array<object> |  |
| `name` | string |  |
| `owner` | object |  |
| `searching` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `GET /contacts/:id` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

