# CoachAccountable: List Companies

Retrieves companies from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-companies?${params}`, {
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
| `includeInactive` | boolean | no | Set to true to include Companies that are marked inactive. Default: `false`. |
| `sortOption` | list | no | One of: `A`, `C`. Default: `C`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "city": "string",
      "country": "string",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "isActive": true,
      "name": "Ava Chen",
      "state": "string",
      "ZIP": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `city` | string |  |
| `country` | string |  |
| `dateAdded` | date |  |
| `ID` | number |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `state` | string |  |
| `ZIP` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

