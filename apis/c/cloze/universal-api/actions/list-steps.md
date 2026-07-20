# Cloze: List Steps

Retrieves steps from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-steps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-steps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-steps?${params}`, {
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
| `segment` | string | no | Project segment filter for steps. |
| `stage` | string | no | Project stage filter for steps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorcode": 1,
      "segments": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success. |
| `segments` | object | Steps grouped by segment key. |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/user/steps` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-steps.md) for the provider-specific parameters and requirements.

