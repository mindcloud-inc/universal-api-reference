# Happy SMS: Get Document



```
GET https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-document?connectionId=$CONNECTION_ID&id=mindcloud-nonexistent-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "mindcloud-nonexistent-doc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-document?${params}`, {
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
| `id` | string | yes | Unique document identifier. Default: `mindcloud-nonexistent-doc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "key": "string",
          "label": "string",
          "type": "string",
          "value": "string"
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
| `[].key` | string | Generated property key. |
| `[].label` | string | Document property label. |
| `[].type` | string | Document property type. |
| `[].value` | string | Document property value. |

## Native endpoint

Through the native Happy SMS API, this operation is `GET /api/v1/protected/domain/custom-data/documents/:id` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

