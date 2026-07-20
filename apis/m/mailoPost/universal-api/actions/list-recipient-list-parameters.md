# MailoPost: List Recipient List Parameters

Retrieves recipient list parameters from MailoPost.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/list-recipient-list-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/list-recipient-list-parameters?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/list-recipient-list-parameters?${params}`, {
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
| `id` | string | yes | MailoPost recipient list identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "kind": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `kind` | string |  |
| `title` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `GET /email/lists/:id/parameters` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recipient-list-parameters.md) for the provider-specific parameters and requirements.

