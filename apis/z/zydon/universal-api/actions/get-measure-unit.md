# Zydon: Get Measure Unit

Retrieves measure unit details from Zydon.

```
GET https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-measure-unit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zydon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-measure-unit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-measure-unit?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "abbreviation": "string",
      "active": true,
      "description": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string | Unit abbreviation. |
| `active` | boolean | Whether the measure unit is active. |
| `description` | string | Unit description. |
| `id` | string | Measure unit identifier. |

## Native endpoint

Through the native Zydon API, this operation is `GET /measure-units/{id}` (base URL `https://api.zydon.com.br/api/sales`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-measure-unit.md) for the provider-specific parameters and requirements.

