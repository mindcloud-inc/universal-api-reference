# Moodo & Moodo AIR: Get Terms And Conditions

Retrieves the Terms and Conditions text from Moodo.

```
GET https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-terms-and-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-terms-and-conditions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-terms-and-conditions?${params}`, {
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
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `GET /terms_and_conditions` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-terms-and-conditions.md) for the provider-specific parameters and requirements.

