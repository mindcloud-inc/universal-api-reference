# eSign Genie: Get Templates by Template IDs

Retrieves templates from eSign Genie by template ID.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-templates-by-template-i-ds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-templates-by-template-i-ds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-templates-by-template-i-ds?${params}`, {
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
      "result": "string",
      "totalTemplates": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `totalTemplates` | number |  |

## Native endpoint

Through the native eSign Genie API, this operation is `POST /templates/templateDetails` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-templates-by-template-i-ds.md) for the provider-specific parameters and requirements.

