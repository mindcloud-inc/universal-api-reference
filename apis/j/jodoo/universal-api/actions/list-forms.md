# Jodoo: List Forms



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-forms?connectionId=$CONNECTION_ID&appId=69c4042cce7f5503d03455c1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "69c4042cce7f5503d03455c1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-forms?${params}`, {
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
| `appId` | string | yes | Jodoo app ID to list forms from. Example: `69c4042cce7f5503d03455c1`. |
| `limit` | number | no | Maximum number of forms to return. Example: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of forms to skip before returning results. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "entryId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `entryId` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /app/entry/list` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

