# Datadog: Get Notebook

Retrieves a notebook from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-notebook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-notebook?connectionId=$CONNECTION_ID&notebookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notebookId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-notebook?${params}`, {
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
| `notebookId` | number | yes | Unique notebook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Notebook returned by the request. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/notebooks/:notebook_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notebook.md) for the provider-specific parameters and requirements.

