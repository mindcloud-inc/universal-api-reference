# e-Gov: Autocomplete Organizations

Finds organizations in e-Gov by partial name.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-organizations?connectionId=$CONNECTION_ID&q=%E7%9C%81" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "省"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-organizations?${params}`, {
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
| `q` | string | yes | Default: `省`. |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /organization_autocomplete` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-organizations.md) for the provider-specific parameters and requirements.

