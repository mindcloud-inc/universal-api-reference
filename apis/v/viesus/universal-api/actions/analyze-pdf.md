# Viesus: Analyze PDF

Analyzes a PDF upload in Viesus.

```
PUT https://connect.mindcloud.co/v1/universal/viesus/latest/actions/analyze-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viesus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viesus/latest/actions/analyze-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viesus/latest/actions/analyze-pdf', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "analyzePdf": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyzePdf` | object | PDF analysis result. |

## Native endpoint

Through the native Viesus API, this operation is `POST /` (base URL `https://api.viesus.cloud/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-pdf.md) for the provider-specific parameters and requirements.

