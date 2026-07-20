# INBOX: Get Import Status

Retrieves an import job status from INBOX.

```
GET https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-import-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a INBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-import-status?connectionId=$CONNECTION_ID&contactListId=string&importId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactListId": "string",
  "importId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-import-status?${params}`, {
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
| `contactListId` | string | yes |  |
| `importId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultCode": 1,
      "resultMessage": "string",
      "resultObject": {},
      "resultStatus": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultCode` | number |  |
| `resultMessage` | string |  |
| `resultObject` | object |  |
| `resultStatus` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native INBOX API, this operation is `GET /inbox/v1/contactlists/:contactListId/import/:importId` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-import-status.md) for the provider-specific parameters and requirements.

