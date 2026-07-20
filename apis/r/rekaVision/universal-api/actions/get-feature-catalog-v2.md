# Reka Vision: Get Feature Catalog (V2)

Retrieves the feature catalog from Reka Vision.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-feature-catalog-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-feature-catalog-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-feature-catalog-v2?${params}`, {
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
      "dependsOn": [
        "string"
      ],
      "description": "string",
      "name": "Ava Chen",
      "note": "string",
      "produces": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dependsOn` | array<string> |  |
| `description` | string |  |
| `name` | string |  |
| `note` | string |  |
| `produces` | array<string> |  |

## Native endpoint

Through the native Reka Vision API, this operation is `GET /v2/features` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature-catalog-v2.md) for the provider-specific parameters and requirements.

