# People Data Labs: Clean Location



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-location?connectionId=$CONNECTION_ID&location=san%20francisco%2C%20california%2C%20united%20states" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "san francisco, california, united states"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-location?${params}`, {
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
| `location` | string | yes | Unformatted location string to standardize into canonical location data. Default: `san francisco, california, united states`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continent": "string",
      "country": "string",
      "geo": "string",
      "locality": "string",
      "metro": "string",
      "name": "Ava Chen",
      "region": "string",
      "status": 1,
      "subregion": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continent` | string |  |
| `country` | string |  |
| `geo` | string |  |
| `locality` | string |  |
| `metro` | string |  |
| `name` | string |  |
| `region` | string |  |
| `status` | number |  |
| `subregion` | string |  |
| `type` | string |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /location/clean` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clean-location.md) for the provider-specific parameters and requirements.

