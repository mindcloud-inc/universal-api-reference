# Zoho Creator: Get Fields

Retrieves fields from a Zoho Creator form.

```
GET https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-fields?connectionId=$CONNECTION_ID&accountOwnerName=Ava%20Chen&appLinkName=https%3A%2F%2Fexample.com&formLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "formLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-fields?${params}`, {
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
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |
| `appLinkName` | string | yes | Zoho Creator app link name. |
| `formLinkName` | string | yes | Zoho Creator form link name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "fields": [
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
| `code` | number | Zoho Creator response code. |
| `fields` | array<object> | Fields defined on the selected Zoho Creator form. |

## Native endpoint

Through the native Zoho Creator API, this operation is `GET /meta/:account_owner_name/:app_link_name/form/:form_link_name/fields` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fields.md) for the provider-specific parameters and requirements.

