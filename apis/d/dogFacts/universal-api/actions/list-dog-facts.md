# Dog Facts: List Dog Facts



```
GET https://connect.mindcloud.co/v1/universal/dogFacts/latest/actions/list-dog-facts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dog Facts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dogFacts/latest/actions/list-dog-facts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dogFacts/latest/actions/list-dog-facts?${params}`, {
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
| `limit` | number | no | Maximum number of random dog facts to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> | Array of returned dog-fact resources. |
| `data[].attributes` | object | Dog-fact resource attributes. |
| `data[].attributes.body` | string | Dog fact text. |
| `data[].id` | string | Dog-fact resource identifier. |
| `data[].type` | string | JSON:API resource type. |

## Native endpoint

Through the native Dog Facts API, this operation is `GET /facts` (base URL `https://dogapi.dog/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dog-facts.md) for the provider-specific parameters and requirements.

