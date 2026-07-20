# Envoice: Delete Estimation

Deletes an existing estimation from Envoice.

```
DELETE https://connect.mindcloud.co/v1/universal/envoice/latest/actions/delete-estimation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/delete-estimation?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/delete-estimation?${params}`, {
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
| `id` | number | yes | Estimation identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number | Deleted estimation identifier. |

## Native endpoint

Through the native Envoice API, this operation is `POST estimation/delete` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-estimation.md) for the provider-specific parameters and requirements.

