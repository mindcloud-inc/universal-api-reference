# Resco Cloud: Delete Multiple Records

Deletes multiple records from Resco Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/delete-multiple-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resco Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/delete-multiple-records?connectionId=$CONNECTION_ID&rawBody=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rawBody": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/delete-multiple-records?${params}`, {
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
| `rawBody` | string | yes | XML Entities body for the Resco DeleteMultiple request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Resco Cloud API returns.

## Native endpoint

Through the native Resco Cloud API, this operation is `POST /DeleteMultiple` (base URL `https://{{credentials.organization}}.app.resco.net/rest/v1/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-records.md) for the provider-specific parameters and requirements.

