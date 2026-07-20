# MoreApp: List Exportable Fields

Retrieves exportable submission fields from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-exportable-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-exportable-fields?connectionId=$CONNECTION_ID&customerId=209321&formId=69bc27abd8b8b4ce5be6b2ba" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321",
  "formId": "69bc27abd8b8b4ce5be6b2ba"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-exportable-fields?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `formId` | string | yes | MoreApp form identifier. Default: `69bc27abd8b8b4ce5be6b2ba`. |

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
| `code` | string | Provider error code for the exportable-fields request. |
| `data` | object | Additional provider error payload. |
| `message` | string | Provider message describing the exportable-fields failure. |
| `traceId` | string | MoreApp trace identifier for support and debugging. |
| `type` | string | Provider error type returned by the exportable-fields endpoint. |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/export/fields` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-exportable-fields.md) for the provider-specific parameters and requirements.

