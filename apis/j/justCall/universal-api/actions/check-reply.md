# JustCall: Check Reply

Checks for a reply in JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/check-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/check-reply?connectionId=$CONNECTION_ID&contactNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/check-reply?${params}`, {
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
| `contactNumber` | string | yes |  |
| `justcallNumber` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `POST /v2.1/texts/checkreply` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-reply.md) for the provider-specific parameters and requirements.

