# Productify.ai: Get Workspace Details



```
GET https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-workspace-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productify.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-workspace-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-workspace-details?${params}`, {
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
      "apiKeyName": "Ava Chen",
      "defaultLanguage": "string",
      "description": "string",
      "heading": "string",
      "isEnterprise": true,
      "modelState": {},
      "name": "Ava Chen",
      "unitOfMeasure": "string",
      "wasSuccessful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyName` | string |  |
| `defaultLanguage` | string |  |
| `description` | string |  |
| `heading` | string |  |
| `isEnterprise` | boolean |  |
| `modelState` | object |  |
| `name` | string |  |
| `unitOfMeasure` | string |  |
| `wasSuccessful` | boolean |  |

## Native endpoint

Through the native Productify.ai API, this operation is `GET /workspace/detail` (base URL `https://api.productify.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-details.md) for the provider-specific parameters and requirements.

