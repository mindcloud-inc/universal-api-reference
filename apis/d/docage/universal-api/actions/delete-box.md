# Docage: Delete Box

Deletes an existing box from Docage.

```
DELETE https://connect.mindcloud.co/v1/universal/docage/latest/actions/delete-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docage/latest/actions/delete-box?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/delete-box?${params}`, {
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
| `id` | string | yes | The Docage box ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Docage API, this operation is `DELETE /Boxes/:id` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-box.md) for the provider-specific parameters and requirements.

