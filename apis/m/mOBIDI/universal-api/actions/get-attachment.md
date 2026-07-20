# MOBIDI: Get Attachment

Retrieves an attachment from a MOBIDI record.

```
GET https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-attachment?connectionId=$CONNECTION_ID&recordId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/get-attachment?${params}`, {
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
| `recordId` | string | yes |  |
| `attachmentId` | string | yes |  |
| `download` | boolean | no | Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOBIDI API returns.

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment.md) for the provider-specific parameters and requirements.

