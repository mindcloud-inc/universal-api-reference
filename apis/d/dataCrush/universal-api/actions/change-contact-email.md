# DataCrush: Search Contacts By Lifecycle

Finds contacts in DataCrush by lifecycle.

```
GET https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/change-contact-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/change-contact-email?connectionId=$CONNECTION_ID&lifecycle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lifecycle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/change-contact-email?${params}`, {
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
| `lifecycle` | string | yes | Lifecycle value to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "rows": [
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
| `result` | string |  |
| `rows` | array<object> |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /contact/search` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-contact-email.md) for the provider-specific parameters and requirements.

