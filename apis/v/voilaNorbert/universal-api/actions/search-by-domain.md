# VoilaNorbert: Search By Domain

Finds contacts in VoilaNorbert by domain or company name.

```
POST https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/search-by-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/search-by-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/search-by-domain', {
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
| `company` | string | no | The company name to search when a domain is not provided. |
| `domain` | string | no | The company domain to search. |
| `listId` | number | no | An optional list id where the found contacts will be attached. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | The result page to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_available": true,
      "has_next": true,
      "result": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_available` | boolean |  |
| `has_next` | boolean |  |
| `result` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `POST /search/domain` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-by-domain.md) for the provider-specific parameters and requirements.

