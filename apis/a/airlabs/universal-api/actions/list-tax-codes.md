# Airlabs: List Tax Codes

Retrieves airline tax codes from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-tax-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-tax-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-tax-codes?${params}`, {
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
      "code": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Tax code. |
| `name` | string | Tax description. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /taxes` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tax-codes.md) for the provider-specific parameters and requirements.

