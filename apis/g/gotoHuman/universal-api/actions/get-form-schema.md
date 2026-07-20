# gotoHuman: Get Form Schema

Retrieves a review form schema from gotoHuman.

```
GET https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/get-form-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gotoHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/get-form-schema?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/get-form-schema?${params}`, {
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
| `formId` | string | yes | The review form ID to fetch the schema for. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `fields` | array<object> | Field schema for the selected review form. |

## Native endpoint

Through the native gotoHuman API, this operation is `GET /fetchSchemaForFormFields` (base URL `https://api.gotohuman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-schema.md) for the provider-specific parameters and requirements.

