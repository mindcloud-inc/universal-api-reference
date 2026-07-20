# Hyperise: Delete Business

Deletes an existing business from Hyperise.

```
DELETE https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/delete-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/delete-business?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/delete-business?${params}`, {
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
| `businessId` | string | yes | The Hyperise business record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rawBody": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rawBody` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Hyperise API, this operation is `DELETE /businesses/:businessId` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-business.md) for the provider-specific parameters and requirements.

