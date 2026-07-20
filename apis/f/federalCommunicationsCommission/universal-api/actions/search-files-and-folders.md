# Federal Communications Commission: Search Files and Folders

Finds FCC OPIF files and folders by search key.

```
GET https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/search-files-and-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/search-files-and-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/search-files-and-folders?${params}`, {
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
| `entityId` | string | no | Unique entity ID. |
| `format` | string | no | Response format. FCC documents json, jsonp, xml. |
| `searchKey` | string | no | Search key for files and folders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "searchResult": {},
      "status": "string",
      "statusCode": 1,
      "statusMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `searchResult` | object | Matching FCC folders and files. |
| `status` | string | FCC Manager response status. |
| `statusCode` | number | FCC Manager response status code. |
| `statusMessage` | string | FCC Manager response message. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `GET /api/manager/search/key/{searchKey}.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-files-and-folders.md) for the provider-specific parameters and requirements.

