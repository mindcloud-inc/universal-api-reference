# Hireflix: Remove Interview Share Link

Deletes a shareable interview link from Hireflix.

```
DELETE https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/remove-interview-share-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/remove-interview-share-link?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/remove-interview-share-link?${params}`, {
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
| `variables.id` | string | yes | The Hireflix interview ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-interview-share-link.md) for the provider-specific parameters and requirements.

