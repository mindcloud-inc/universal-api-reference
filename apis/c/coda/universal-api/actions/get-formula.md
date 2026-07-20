# Coda: Get Formula

Retrieves formula details from a Coda doc.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-formula
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-formula?connectionId=$CONNECTION_ID&docId=string&formulaIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "formulaIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-formula?${params}`, {
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
| `docId` | list | yes |  |
| `formulaIdOrName` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "parent": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "type": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `parent.browserLink` | string |  |
| `parent.href` | string |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `parent.type` | string |  |
| `type` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/formulas/:formulaIdOrName` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-formula.md) for the provider-specific parameters and requirements.

