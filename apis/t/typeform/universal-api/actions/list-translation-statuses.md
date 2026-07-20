# Typeform: List Translation Statuses



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-translation-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-translation-statuses?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-translation-statuses?${params}`, {
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
| `formId` | string | yes | Typeform form identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "languages": [
        {
          "code": "string",
          "isMain": true,
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `languages` | array<object> | Language statuses for the form translation set. |
| `languages[].code` | string | Language code. |
| `languages[].isMain` | boolean | Whether this is the form main language. |
| `languages[].status` | string | Translation status for this language. |

## Native endpoint

Through the native Typeform API, this operation is `GET /forms/:formId/translations/status` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-translation-statuses.md) for the provider-specific parameters and requirements.

