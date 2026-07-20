# Refiner: Delete Form

Archives an existing form in Refiner.

```
DELETE https://connect.mindcloud.co/v1/universal/refiner/latest/actions/delete-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/delete-form?connectionId=$CONNECTION_ID&formUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/delete-form?${params}`, {
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
| `formUuid` | string | yes | The form UUID to archive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `DELETE /forms` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form.md) for the provider-specific parameters and requirements.

