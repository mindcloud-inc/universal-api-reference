# Cloutly: Get Business

Retrieves business details from the Cloutly marketplace.

```
GET https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/get-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloutly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/get-business?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/get-business?${params}`, {
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
| `businessId` | string | yes | Business ID from Cloutly. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Cloutly API, this operation is `GET https://marketplace.cloutly.com/api/v2/businesses/:businessId` (base URL `https://app.cloutly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business.md) for the provider-specific parameters and requirements.

