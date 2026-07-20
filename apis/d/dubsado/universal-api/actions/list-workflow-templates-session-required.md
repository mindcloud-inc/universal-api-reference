# Dubsado: List Workflow Templates (Session Required)



```
GET https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-workflow-templates-session-required
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubsado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-workflow-templates-session-required?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-workflow-templates-session-required?${params}`, {
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
| `sortBy` | string | no | Optional sort key observed in the Dubsado app bundle for /workflow/template reads. |
| `limit` | number | no | Optional result limit observed in the Dubsado app bundle for /workflow/template reads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": "string",
      "index": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `index` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Dubsado API, this operation is `GET /workflow/template` (base URL `https://app.dubsado.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-templates-session-required.md) for the provider-specific parameters and requirements.

