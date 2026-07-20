# Zoho People: List Forms

Retrieves forms from Zoho People.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/list-forms?${params}`, {
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
      "componentId": 1,
      "displayName": "Ava Chen",
      "formLinkName": "https://example.com",
      "iscustom": true,
      "isVisible": true,
      "permissionDetails": {
        "add": 1,
        "edit": 1,
        "view": 1
      },
      "viewDetails": {
        "viewId": 1,
        "viewName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `componentId` | number |  |
| `displayName` | string |  |
| `formLinkName` | string |  |
| `iscustom` | boolean |  |
| `isVisible` | boolean |  |
| `permissionDetails.add` | number |  |
| `permissionDetails.edit` | number |  |
| `permissionDetails.view` | number |  |
| `viewDetails.viewId` | number |  |
| `viewDetails.viewName` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/forms` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

