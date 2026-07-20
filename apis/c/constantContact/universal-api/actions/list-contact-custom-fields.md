# Constant Contact: List Contact Custom Fields

Retrieves contact custom fields from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-custom-fields?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Number of results per page (1-100). Example: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {}
      ],
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> |  |
| `links` | object |  |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /contact_custom_fields` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-custom-fields.md) for the provider-specific parameters and requirements.

