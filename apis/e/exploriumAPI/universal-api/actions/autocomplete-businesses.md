# Explorium: Autocomplete Businesses

Retrieves business autocomplete results from Explorium API.

```
GET https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/autocomplete-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/autocomplete-businesses?connectionId=$CONNECTION_ID&field=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/autocomplete-businesses?${params}`, {
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
| `field` | string | yes | The autocomplete field to query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseContext` | object | Explorium response metadata. |

## Native endpoint

Through the native Explorium API, this operation is `GET /v1/businesses/autocomplete` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-businesses.md) for the provider-specific parameters and requirements.

