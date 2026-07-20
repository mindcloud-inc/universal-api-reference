# Agilite: Get Keyword Value By Label

Retrieves a keyword value from Agilite by profile and label key.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-value-by-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-value-by-label?connectionId=$CONNECTION_ID&profileKey=string&labelKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileKey": "string",
  "labelKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-keyword-value-by-label?${params}`, {
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
| `labelKey` | string | yes | Keyword label key to resolve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Resolved keyword value. |

## Native endpoint

Through the native Agilite API, this operation is `GET /keywords/getValueByLabel` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keyword-value-by-label.md) for the provider-specific parameters and requirements.

