# Brevo: List Contact Attributes



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-contact-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-contact-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-contact-attributes?${params}`, {
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
      "attributes": [
        {
          "calculatedValue": "string",
          "category": "string",
          "name": "Ava Chen",
          "type": "string"
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
| `attributes[].calculatedValue` | string |  |
| `attributes[].category` | string |  |
| `attributes[].name` | string |  |
| `attributes[].type` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts/attributes` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-attributes.md) for the provider-specific parameters and requirements.

