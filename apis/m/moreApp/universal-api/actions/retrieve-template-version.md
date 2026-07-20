# MoreApp: Retrieve Template Version

Retrieves a template version from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-template-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-template-version?connectionId=$CONNECTION_ID&customerId=1&formId=string&formVersionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "formId": "string",
  "formVersionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-template-version?${params}`, {
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
| `customerId` | number | yes |  |
| `formId` | string | yes |  |
| `formVersionId` | string | yes |  |
| `brandingId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "message": "string",
      "traceId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `message` | string |  |
| `traceId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/{{formVersionId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-template-version.md) for the provider-specific parameters and requirements.

