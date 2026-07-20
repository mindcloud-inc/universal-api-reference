# Zippopotamus: List Postal Codes by Place

Retrieves postal codes in Zippopotamus by place name.

```
GET https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-postal-codes-by-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zippopotamus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-postal-codes-by-place?connectionId=$CONNECTION_ID&country=US&state=MA&place=Belmont" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "US",
  "state": "MA",
  "place": "Belmont"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zippopotamus/latest/actions/list-postal-codes-by-place?${params}`, {
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
| `country` | string | yes | ISO 3166-1 alpha-2 country code, such as US. Example: `US`. |
| `state` | string | yes | Two-letter state or province abbreviation, such as MA. Example: `MA`. |
| `place` | string | yes | Place name, such as Belmont. Example: `Belmont`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "country abbreviation": "string",
      "place name": "Ava Chen",
      "places": [
        {}
      ],
      "state": "string",
      "state abbreviation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `country abbreviation` | string |  |
| `place name` | string |  |
| `places` | array<object> |  |
| `state` | string |  |
| `state abbreviation` | string |  |

## Native endpoint

Through the native Zippopotamus API, this operation is `GET /{{country}}/{{state}}/{{place}}` (base URL `https://api.zippopotam.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-postal-codes-by-place.md) for the provider-specific parameters and requirements.

