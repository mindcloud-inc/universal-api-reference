# EDEN AI: List Features

Retrieves available features from EDEN AI.

```
GET https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EDEN AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-features?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-features?${params}`, {
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
      "features": [
        {
          "description": "string",
          "fullname": "Ava Chen",
          "name": "Ava Chen",
          "subfeatures": [
            {
              "fullname": "Ava Chen",
              "mode": "string",
              "models": [
                {}
              ],
              "name": "Ava Chen"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `features` | array<object> | Available Eden AI feature categories. |
| `features[].description` | string | Feature category description when provided. |
| `features[].fullname` | string | Human-readable feature category name. |
| `features[].name` | string | Feature category key used in the info API paths. |
| `features[].subfeatures` | array<object> | Supported subfeatures in the category. |
| `features[].subfeatures[].fullname` | string | Human-readable subfeature name. |
| `features[].subfeatures[].mode` | string | Execution mode for the subfeature, such as sync or async. |
| `features[].subfeatures[].models` | array<object> | Provider models available for the subfeature. |
| `features[].subfeatures[].name` | string | Subfeature key used in the info API paths. |

## Native endpoint

Through the native EDEN AI API, this operation is `GET /info` (base URL `https://api.edenai.run/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-features.md) for the provider-specific parameters and requirements.

