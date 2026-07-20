# Kite Suite: Get Form Theme Templates



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-form-theme-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-form-theme-templates?connectionId=$CONNECTION_ID&layout=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "layout": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-form-theme-templates?${params}`, {
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
| `layout` | string | yes | Layout type to filter templates |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "isLive": true,
      "layout": "string",
      "previewImage": {},
      "themeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The template ID |
| `isLive` | boolean | Whether the template is available for use |
| `layout` | string | Layout type of the form |
| `previewImage` | object |  |
| `themeName` | string | Name of the theme |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/form-theme` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-theme-templates.md) for the provider-specific parameters and requirements.

