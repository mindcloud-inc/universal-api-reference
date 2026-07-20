# DocuPipe: Get Standardization Count

Retrieves the standardization count from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-standardization-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-standardization-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-standardization-count?${params}`, {
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
      "schemaNames": [
        "Ava Chen"
      ],
      "totalStandardizations": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `schemaNames` | array<string> | List of schema names. |
| `totalStandardizations` | number | Total number of standardizations. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /standardizations/summary` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-standardization-count.md) for the provider-specific parameters and requirements.

