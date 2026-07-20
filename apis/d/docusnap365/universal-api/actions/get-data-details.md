# Docusnap365: Get Data Details



```
GET https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/get-data-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docusnap365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/get-data-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docusnap365/latest/actions/get-data-details?${params}`, {
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
| `id` | string | yes | The Docusnap365 data ID to fetch in detailed form. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docusnap365 API returns.

## Native endpoint

Through the native Docusnap365 API, this operation is `GET /api/v2/segment/data/:id/detailed` (base URL `https://api.docusnap365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-details.md) for the provider-specific parameters and requirements.

