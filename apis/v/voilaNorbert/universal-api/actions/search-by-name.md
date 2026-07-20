# VoilaNorbert: Search By Name

Finds a contact in VoilaNorbert by full name and domain.

```
POST https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/search-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/search-by-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/search-by-name', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Company domain for the search. |
| `name` | string | no | Full name of the person to search. |

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
      "is_new": true,
      "lists": [
        {}
      ],
      "name": "Ava Chen",
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
| `is_new` | boolean |  |
| `lists` | array<object> |  |
| `name` | string |  |
| `searching` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `POST /search/name` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-by-name.md) for the provider-specific parameters and requirements.

