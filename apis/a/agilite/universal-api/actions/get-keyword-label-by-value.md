# Agilite: Get Keyword Label By Value

Retrieves a keyword label from Agilite by profile and value key.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-label-by-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-label-by-value?connectionId=$CONNECTION_ID&profileKey=string&valueKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileKey": "string",
  "valueKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-label-by-value?${params}`, {
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
| `profileKey` | string | yes | Agilit-e keyword profile key. |
| `valueKey` | string | yes | Keyword value key to resolve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Resolved keyword label. |

## Native endpoint

Through the native Agilite API, this operation is `GET /keywords/getLabelByValue` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keyword-label-by-value.md) for the provider-specific parameters and requirements.

