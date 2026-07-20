# PPM Express: Get Portfolio



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-portfolio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-portfolio?connectionId=$CONNECTION_ID&id=a91cebee-6b3a-4b97-802a-aa68c7857a0c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "a91cebee-6b3a-4b97-802a-aa68c7857a0c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/get-portfolio?${params}`, {
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
| `id` | string | yes | The portfolio ID to fetch. Default: `a91cebee-6b3a-4b97-802a-aa68c7857a0c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The requested portfolio record. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/portfolios/:id` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portfolio.md) for the provider-specific parameters and requirements.

