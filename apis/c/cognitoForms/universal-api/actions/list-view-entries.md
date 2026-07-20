# Cognito Forms: List View Entries



```
GET https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/list-view-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/list-view-entries?connectionId=$CONNECTION_ID&formId=string&viewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "viewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/list-view-entries?${params}`, {
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
| `formId` | string | yes |  |
| `viewId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "odataContext": "string",
      "value": [
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
| `odataContext` | string | OData context URL for the entry list. |
| `value` | array<object> | Entries returned by the view query. |

## Native endpoint

Through the native Cognito Forms API, this operation is `GET /odata/Forms(:formId)/Views(:viewId)/Entries` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-view-entries.md) for the provider-specific parameters and requirements.

