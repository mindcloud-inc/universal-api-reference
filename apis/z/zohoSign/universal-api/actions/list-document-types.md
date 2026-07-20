# Zoho Sign: List Document Types

Retrieves document types from Zoho Sign.

```
GET https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-document-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-document-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-document-types?${params}`, {
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
      "requestTypeDescription": "string",
      "requestTypeId": "string",
      "requestTypeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestTypeDescription` | string |  |
| `requestTypeId` | string |  |
| `requestTypeName` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `GET /requesttypes` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-types.md) for the provider-specific parameters and requirements.

