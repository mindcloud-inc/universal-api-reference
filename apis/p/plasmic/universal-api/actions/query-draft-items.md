# Plasmic: Query Draft Items

Retrieves draft items from Plasmic CMS.

```
GET https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/query-draft-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plasmic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/query-draft-items?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/query-draft-items?${params}`, {
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
| `modelId` | string | yes | The Plasmic CMS model identifier to query in draft mode. |
| `q` | string | no | A JSON-encoded Plasmic query object used to constrain draft rows. |
| `locale` | string | no | Optional locale tag such as ar-JO. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rows` | array<object> | The queried Plasmic CMS draft rows. |

## Native endpoint

Through the native Plasmic API, this operation is `GET /databases/{{credentials.cmsId}}/tables/:modelId/query` (base URL `https://data.plasmic.app/api/v1/cms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-draft-items.md) for the provider-specific parameters and requirements.

