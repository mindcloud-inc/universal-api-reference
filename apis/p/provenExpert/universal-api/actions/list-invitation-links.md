# ProvenExpert: List Invitation Links

Lists survey invitation links in ProvenExpert.

```
GET https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-invitation-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-invitation-links?connectionId=$CONNECTION_ID&data.code=VRTQ13" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data.code": "VRTQ13"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/list-invitation-links?${params}`, {
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
| `data.code` | string | yes | Survey code whose invitation links should be listed. Example: `VRTQ13`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "email": "ava@example.com",
      "rated": 1,
      "url": "https://example.com",
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Unix timestamp for when the invitation link was created. |
| `email` | string | Evaluator email address tied to the invitation link. |
| `rated` | number | Whether an evaluation has already been submitted through the invitation link. |
| `url` | string | Personalized invitation link. |
| `used` | number | Whether the invitation link has already been clicked. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /invite/url/get` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invitation-links.md) for the provider-specific parameters and requirements.

