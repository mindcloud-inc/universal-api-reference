# Brand.dev: Retrieve NAICS Code for Any Brand

Retrieves a NAICS code for a brand in Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/retrieve-naics-code-for-any-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/retrieve-naics-code-for-any-brand?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/retrieve-naics-code-for-any-brand?${params}`, {
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
| `input` | string | yes | Brand name or domain to classify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codes": [
        [
          {}
        ]
      ],
      "domain": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codes[]` | array<object> |  |
| `codes[].code` | string |  |
| `codes[].confidence` | string |  |
| `codes[].name` | string |  |
| `domain` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /brand/naics` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-naics-code-for-any-brand.md) for the provider-specific parameters and requirements.

