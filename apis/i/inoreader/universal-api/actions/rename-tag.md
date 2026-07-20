# Inoreader: Rename Tag

Renames an existing tag in Inoreader.

```
PUT https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/rename-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/rename-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceTag": "string",
  "targetName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/rename-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceTag": "string",
    "targetName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceTag` | string | yes | Full source tag or folder name, for example user/-/label/Tech. |
| `targetName` | string | yes | New tag or folder name without forward slashes. |

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
| `response` | string | Provider acknowledgement returned by Inoreader for the rename-tag mutation. |

## Native endpoint

Through the native Inoreader API, this operation is `POST /rename-tag` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-tag.md) for the provider-specific parameters and requirements.

