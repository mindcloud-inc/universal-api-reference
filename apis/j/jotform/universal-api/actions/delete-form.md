# Jotform: Delete Form

Deletes an existing form from Jotform.

```
DELETE https://connect.mindcloud.co/v1/universal/jotform/latest/actions/delete-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/delete-form?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/delete-form?${params}`, {
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
| `formId` | string | yes | Form ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted form ID. |
| `status` | string | Form status after delete. |
| `title` | string | Form title. |
| `updated_at` | string | Update timestamp. |

## Native endpoint

Through the native Jotform API, this operation is `DELETE /form/:formId` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form.md) for the provider-specific parameters and requirements.

