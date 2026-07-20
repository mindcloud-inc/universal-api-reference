# Cohere: Get Dataset Usage

Retrieves dataset usage details from Cohere.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-dataset-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-dataset-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/get-dataset-usage?${params}`, {
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
      "datasetCount": 1,
      "organizationUsage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasetCount` | number |  |
| `organizationUsage` | number |  |

## Native endpoint

Through the native Cohere API, this operation is `GET /v1/datasets/usage` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset-usage.md) for the provider-specific parameters and requirements.

