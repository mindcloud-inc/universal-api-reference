# Filestage: Get File URL

Retrieves a file URL from Filestage by version.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-file-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-file-url?connectionId=$CONNECTION_ID&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-file-url?${params}`, {
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
| `versionId` | string | yes | Version id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "original": "string",
      "transcodedPdf": "string",
      "xod": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `original` | string |  |
| `transcodedPdf` | string |  |
| `xod` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `GET /versions/{versionId}/fileDatas/url` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-url.md) for the provider-specific parameters and requirements.

