# Verificaremails: Get All Credits

Retrieves available credits for all Verificaremails services.

```
GET https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-all-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verificaremails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-all-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/get-all-credits?${params}`, {
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
      "apiService": "string",
      "apiServiceAlias": "string",
      "credits": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiService` | string | API service code for the credit balance entry. |
| `apiServiceAlias` | string | Human-readable service name for the credit balance entry. |
| `credits` | string | Available credits for the listed API service. |

## Native endpoint

Through the native Verificaremails API, this operation is `GET /all/credits` (base URL `https://dashboard.verificaremails.com/myapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-credits.md) for the provider-specific parameters and requirements.

