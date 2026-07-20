# Zenkit: Delete Deprecated Entry

Deletes a deprecated item from Zenkit.

```
DELETE https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/delete-deprecated-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/delete-deprecated-entry?connectionId=$CONNECTION_ID&entryAllId=string&listAllId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entryAllId": "string",
  "listAllId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/delete-deprecated-entry?${params}`, {
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
| `entryAllId` | string | yes | The entry all id |
| `listAllId` | string | yes | The list all id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": {
        "id": 1,
        "listId": 1,
        "shortId": "string",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry.id` | number |  |
| `entry.listId` | number |  |
| `entry.shortId` | string |  |
| `entry.uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `DELETE /lists/:listAllId/deprecated-entries/:entryAllId` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-deprecated-entry.md) for the provider-specific parameters and requirements.

