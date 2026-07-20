# Jotform: Get Form Property

Retrieves a form property from Jotform.

```
GET https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-form-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-form-property?connectionId=$CONNECTION_ID&formId=string&propertyKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "propertyKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-form-property?${params}`, {
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
| `formId` | string | yes | Form ID |
| `propertyKey` | string | yes | Property key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeRedirect": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeRedirect` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `GET /form/:formId/properties/:propertyKey` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-property.md) for the provider-specific parameters and requirements.

