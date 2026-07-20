# Kontent.ai: Retrieve content type element

Retrieves a content type element from Kontent.ai.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-content-type-element
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-content-type-element?connectionId=$CONNECTION_ID&environmentId=string&typeCodename=Ava%20Chen&elementCodename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentId": "string",
  "typeCodename": "Ava Chen",
  "elementCodename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-content-type-element?${params}`, {
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
| `environmentId` | string | yes | Kontent.ai project environment identifier. |
| `typeCodename` | string | yes | Content type codename. |
| `elementCodename` | string | yes | Content type element codename. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codename": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codename` | string | Element codename. |
| `id` | string | Element ID. |
| `name` | string | Element name. |
| `type` | string | Element type. |

## Native endpoint

Through the native Kontent.ai API, this operation is `GET /:environment_id/types/:type_codename/elements/:element_codename` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-content-type-element.md) for the provider-specific parameters and requirements.

