# Hunter: Discover Companies



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/discover-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/discover-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/discover-companies?${params}`, {
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
| `query` | string | no |  |
| `organization` | object | no |  |
| `similarTo` | string | no |  |
| `headquartersLocation` | object | no |  |
| `industry` | object | no |  |
| `headcount` | string | no |  |
| `companyType` | object | no |  |
| `yearFounded` | object | no |  |
| `keywords` | object | no |  |
| `technology` | object | no |  |
| `funding` | object | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "emailsCount": {},
      "organization": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `emailsCount` | object |  |
| `organization` | string |  |

## Native endpoint

Through the native Hunter API, this operation is `POST /discover` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discover-companies.md) for the provider-specific parameters and requirements.

