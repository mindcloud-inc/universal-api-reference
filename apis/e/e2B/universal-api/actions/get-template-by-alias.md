# E2B: Get Template By Alias

Finds a template in E2B by alias.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-template-by-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-template-by-alias?connectionId=$CONNECTION_ID&alias=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alias": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-template-by-alias?${params}`, {
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
| `alias` | string | yes | Template alias to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "public": true,
      "templateID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `public` | boolean | Whether the template is public. |
| `templateID` | string | Identifier of the template. |

## Native endpoint

Through the native E2B API, this operation is `GET /templates/aliases/{alias}` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-by-alias.md) for the provider-specific parameters and requirements.

