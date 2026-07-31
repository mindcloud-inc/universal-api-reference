# FOAAS: Back Off



```
GET https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/back-off
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FOAAS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/back-off?connectionId=$CONNECTION_ID&name=Ava%20Chen&from=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "from": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/back-off?${params}`, {
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
| `name` | string | yes |  |
| `from` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "subtitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `subtitle` | string |  |

## Native endpoint

Through the native FOAAS API, this operation is `GET /back/:name/:from` (base URL `https://foaas.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/back-off.md) for the provider-specific parameters and requirements.

