# e-Gov: Autocomplete Formats

Finds resource formats in e-Gov by partial name.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-formats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-formats?connectionId=$CONNECTION_ID&q=csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "csv"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-formats?${params}`, {
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
| `q` | string | yes | Default: `csv`. |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /format_autocomplete` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-formats.md) for the provider-specific parameters and requirements.

