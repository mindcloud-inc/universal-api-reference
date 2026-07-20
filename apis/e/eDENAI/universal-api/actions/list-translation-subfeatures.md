# EDEN AI: List Translation Subfeatures

Retrieves available translation subfeatures from EDEN AI.

```
GET https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-translation-subfeatures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EDEN AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-translation-subfeatures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-translation-subfeatures?${params}`, {
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
      "description": "string",
      "fullname": "Ava Chen",
      "name": "Ava Chen",
      "subfeatures": [
        {
          "description": "string",
          "fullname": "Ava Chen",
          "mode": "string",
          "models": [
            {}
          ],
          "name": "Ava Chen"
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
| `description` | string | Feature category description. |
| `fullname` | string | Feature category display name. |
| `name` | string | Feature category key. |
| `subfeatures` | array<object> | Subfeatures available in this category. |
| `subfeatures[].description` | string | Subfeature description. |
| `subfeatures[].fullname` | string | Subfeature display name. |
| `subfeatures[].mode` | string | Execution mode for the subfeature. |
| `subfeatures[].models` | array<object> | Models available for the subfeature. |
| `subfeatures[].name` | string | Subfeature key. |

## Native endpoint

Through the native EDEN AI API, this operation is `GET /info/translation` (base URL `https://api.edenai.run/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-translation-subfeatures.md) for the provider-specific parameters and requirements.

