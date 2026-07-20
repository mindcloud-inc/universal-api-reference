# PageVitals: Get Page Network Chart



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-network-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-network-chart?connectionId=$CONNECTION_ID&websiteId=string&pageId=string&device=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "pageId": "string",
  "device": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-network-chart?${params}`, {
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
| `websiteId` | string | yes |  |
| `pageId` | string | yes |  |
| `device` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytesCss": 1,
      "bytesDoc": 1,
      "bytesFont": 1,
      "bytesImage": 1,
      "bytesJs": 1,
      "bytesMedia": 1,
      "bytesOther": 1,
      "bytesThirdparty": 1,
      "bytesTotal": 1,
      "date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytesCss` | number |  |
| `bytesDoc` | number |  |
| `bytesFont` | number |  |
| `bytesImage` | number |  |
| `bytesJs` | number |  |
| `bytesMedia` | number |  |
| `bytesOther` | number |  |
| `bytesThirdparty` | number |  |
| `bytesTotal` | number |  |
| `date` | string |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/pages/:pageId/network` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-network-chart.md) for the provider-specific parameters and requirements.

