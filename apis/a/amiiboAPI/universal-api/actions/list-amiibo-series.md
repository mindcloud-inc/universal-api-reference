# Amiibo API: List Amiibo Series



```
GET https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/list-amiibo-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amiibo API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/list-amiibo-series?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/list-amiibo-series?${params}`, {
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
| `name` | string | no | Optional series name filter. |
| `sort` | string | no | Comma-separated source-defined fields: key or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amiibo": [
        {
          "key": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amiibo` | array<object> | Native AmiiboAPI metadata envelope. |
| `amiibo[].key` | string | Hexadecimal metadata key. |
| `amiibo[].name` | string | Metadata name. |

## Native endpoint

Through the native Amiibo API API, this operation is `GET /api/amiiboseries/` (base URL `https://amiiboapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-amiibo-series.md) for the provider-specific parameters and requirements.

