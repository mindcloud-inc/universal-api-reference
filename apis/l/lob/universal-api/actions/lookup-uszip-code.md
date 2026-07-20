# Lob: Lookup US ZIP Code



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/lookup-uszip-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/lookup-uszip-code?connectionId=$CONNECTION_ID&zipCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zipCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/lookup-uszip-code?${params}`, {
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
| `zipCode` | string | yes | 5-digit US ZIP code to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cities": [
        {}
      ],
      "id": "string",
      "object": "string",
      "zip_code": "string",
      "zip_code_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cities` | array<object> |  |
| `id` | string |  |
| `object` | string |  |
| `zip_code` | string |  |
| `zip_code_type` | string |  |

## Native endpoint

Through the native Lob API, this operation is `POST /us_zip_lookups` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-uszip-code.md) for the provider-specific parameters and requirements.

