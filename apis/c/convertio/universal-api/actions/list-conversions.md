# Convertio: List Conversions

Retrieves conversions and statuses from Convertio.

```
GET https://connect.mindcloud.co/v1/universal/convertio/latest/actions/list-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convertio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertio/latest/actions/list-conversions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertio/latest/actions/list-conversions?${params}`, {
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
| `count` | number | no | Number of latest conversion records to return. |
| `status` | string | no | Filter by conversion status. Default: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Convertio API, this operation is `POST /convert/list` (base URL `https://api.convertio.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversions.md) for the provider-specific parameters and requirements.

