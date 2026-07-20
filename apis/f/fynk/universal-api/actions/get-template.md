# fynk: Get Template

Retrieves detailed template information from fynk.

```
GET https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-template?connectionId=$CONNECTION_ID&template=11111111-1111-1111-1111-111111111111" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template": "11111111-1111-1111-1111-111111111111"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-template?${params}`, {
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
| `template` | string | yes | The template UUID. Default: `11111111-1111-1111-1111-111111111111`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native fynk API, this operation is `GET /templates/:template` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

