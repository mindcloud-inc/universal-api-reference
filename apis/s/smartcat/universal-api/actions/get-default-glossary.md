# Smartcat: Get Default Glossary

Retrieves the default glossary from the Smartcat account.

```
GET https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-default-glossary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-default-glossary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-default-glossary?${params}`, {
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
      "id": "string",
      "isDefault": true,
      "languages": [
        "string"
      ],
      "name": "Ava Chen",
      "units": 1,
      "unitsPending": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isDefault` | boolean |  |
| `languages` | array<string> |  |
| `name` | string |  |
| `units` | number |  |
| `unitsPending` | number |  |

## Native endpoint

Through the native Smartcat API, this operation is `GET /api/integration/v1/glossaries/default` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-glossary.md) for the provider-specific parameters and requirements.

