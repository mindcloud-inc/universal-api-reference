# AbcSubmit: Get Form JS Embed Code

Retrieves JavaScript embed code for an AbcSubmit form.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-js-embed-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-js-embed-code?connectionId=$CONNECTION_ID&formId=string&seoFormName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "seoFormName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-js-embed-code?${params}`, {
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
| `formId` | string | yes | The ID of the form to embed. |
| `seoFormName` | string | yes | The SEO form slug used in the embed script URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `GET /embed/:form_id/:seo_form_name.js` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-js-embed-code.md) for the provider-specific parameters and requirements.

