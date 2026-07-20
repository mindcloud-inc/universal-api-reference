# Global Patron: Retrieve Form JSON

Retrieves form JSON from Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-form-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-form-json?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-form-json?${params}`, {
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
| `formId` | string | yes | ID of the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formDefinition": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formDefinition` | object | JSON definition of the form for rendering. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/form/{formId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-form-json.md) for the provider-specific parameters and requirements.

