# OTO: List Cities

Retrieves cities from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-cities?connectionId=$CONNECTION_ID&country=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-cities?${params}`, {
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
| `country` | string | yes | Two-letter country code to list cities for. |
| `perPage` | number | no | Maximum number of cities to return per page. Default: `10`. |
| `page` | number | no | Page number to fetch. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getCities": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getCities` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native OTO API, this operation is `POST /getCities` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cities.md) for the provider-specific parameters and requirements.

