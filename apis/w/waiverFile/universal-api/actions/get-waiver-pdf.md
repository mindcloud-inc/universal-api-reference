# WaiverFile: Get Waiver PDF

Retrieves a waiver PDF from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-waiver-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-waiver-pdf?connectionId=$CONNECTION_ID&waiverID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "waiverID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-waiver-pdf?${params}`, {
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
| `waiverID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaiverFile API returns.

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetWaiverPDF` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-waiver-pdf.md) for the provider-specific parameters and requirements.

