# Persona: Retrieve Inquiry Template



```
GET https://connect.mindcloud.co/v1/universal/persona/latest/actions/retrieve-inquiry-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Persona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/persona/latest/actions/retrieve-inquiry-template?connectionId=$CONNECTION_ID&inquiryTemplateId=itmpl_5bfQzkXkK12o7bBh5W82YzuYv77M" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inquiryTemplateId": "itmpl_5bfQzkXkK12o7bBh5W82YzuYv77M"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/persona/latest/actions/retrieve-inquiry-template?${params}`, {
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
| `inquiryTemplateId` | string | yes | Inquiry Template ID Example: `itmpl_5bfQzkXkK12o7bBh5W82YzuYv77M`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Persona API returns.

## Native endpoint

Through the native Persona API, this operation is `GET /inquiry-templates/[:inquiry-template-id]` (base URL `https://api.withpersona.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-inquiry-template.md) for the provider-specific parameters and requirements.

