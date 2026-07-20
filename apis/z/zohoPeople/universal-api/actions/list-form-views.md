# Zoho People: List Form Views

Retrieves views for a Zoho People form.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-form-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-form-views?connectionId=$CONNECTION_ID&formLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-form-views?${params}`, {
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
| `formLinkName` | string | yes | Zoho People formLinkName. Example: employee. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "isDefaultView": true,
      "isUserDefaultView": true,
      "viewId": "string",
      "viewName": "Ava Chen",
      "viewType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `isDefaultView` | boolean |  |
| `isUserDefaultView` | boolean |  |
| `viewId` | string |  |
| `viewName` | string |  |
| `viewType` | number |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/forms/:formLinkName/views` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-views.md) for the provider-specific parameters and requirements.

