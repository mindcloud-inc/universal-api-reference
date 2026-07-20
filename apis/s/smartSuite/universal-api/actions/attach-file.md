# SmartSuite: Attach File

Attaches a file to a SmartSuite record.

```
PUT https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/attach-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/attach-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "69b45da87cb40fc74dbb4b84",
  "recordId": "69b853498535da13ccf41722",
  "fileFieldSlug": "sbbb132dec",
  "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/attach-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "69b45da87cb40fc74dbb4b84",
    "recordId": "69b853498535da13ccf41722",
    "fileFieldSlug": "sbbb132dec",
    "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | The SmartSuite table ID containing the target record. Example: `69b45da87cb40fc74dbb4b84`. |
| `recordId` | string | yes | The SmartSuite record ID to update with the file attachment. Example: `69b853498535da13ccf41722`. |
| `fileFieldSlug` | string | yes | The file field slug that should receive the attached file URL. Example: `sbbb132dec`. |
| `fileUrl` | string | yes | A publicly reachable file URL for SmartSuite to fetch and attach. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "applicationSlug": "string",
      "autonumber": 1,
      "commentsCount": 1,
      "deletedBy": {},
      "deletedDate": {
        "date": {},
        "includeTime": true
      },
      "description": "string",
      "firstCreated": {
        "by": "string",
        "on": "string"
      },
      "id": "string",
      "lastUpdated": {
        "by": "string",
        "on": "string"
      },
      "mctestfld1": "string",
      "ranking": {
        "default": "string"
      },
      "s1a2bf428a": "string",
      "s6730fc612": {
        "date": {},
        "includeTime": true
      },
      "s79d05d2c0": {
        "updatedOn": {},
        "value": "string"
      },
      "s7f68e16a2": {},
      "s9920bb125": {
        "completedItems": 1,
        "totalItems": 1
      },
      "sa6bf27e4f": "string",
      "sbbb132dec": [
        {
          "convertedVideoHandle": "string",
          "createdOn": "string",
          "description": "string",
          "fileType": "string",
          "handle": "string",
          "icon": "string",
          "metadata": {
            "container": "string",
            "filename": "Ava Chen",
            "key": "string",
            "mimetype": "string",
            "size": 1
          },
          "updatedOn": "string",
          "videoConversionStatus": "string",
          "videoThumbnailHandle": "string"
        }
      ],
      "sc03076770": {},
      "se57bd1da2": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationId` | string |  |
| `applicationSlug` | string |  |
| `autonumber` | number |  |
| `commentsCount` | number |  |
| `deletedBy` | object |  |
| `deletedDate.date` | object |  |
| `deletedDate.includeTime` | boolean |  |
| `description` | string |  |
| `firstCreated.by` | string |  |
| `firstCreated.on` | string |  |
| `id` | string |  |
| `lastUpdated.by` | string |  |
| `lastUpdated.on` | string |  |
| `mctestfld1` | string |  |
| `ranking.default` | string |  |
| `s1a2bf428a` | string |  |
| `s6730fc612.date` | object |  |
| `s6730fc612.includeTime` | boolean |  |
| `s79d05d2c0.updatedOn` | object |  |
| `s79d05d2c0.value` | string |  |
| `s7f68e16a2` | object |  |
| `s9920bb125.completedItems` | number |  |
| `s9920bb125.totalItems` | number |  |
| `sa6bf27e4f` | string |  |
| `sbbb132dec[].convertedVideoHandle` | string |  |
| `sbbb132dec[].createdOn` | string |  |
| `sbbb132dec[].description` | string |  |
| `sbbb132dec[].fileType` | string |  |
| `sbbb132dec[].handle` | string |  |
| `sbbb132dec[].icon` | string |  |
| `sbbb132dec[].metadata.container` | string |  |
| `sbbb132dec[].metadata.filename` | string |  |
| `sbbb132dec[].metadata.key` | string |  |
| `sbbb132dec[].metadata.mimetype` | string |  |
| `sbbb132dec[].metadata.size` | number |  |
| `sbbb132dec[].updatedOn` | string |  |
| `sbbb132dec[].videoConversionStatus` | string |  |
| `sbbb132dec[].videoThumbnailHandle` | string |  |
| `sc03076770` | object |  |
| `se57bd1da2` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `PATCH /applications/:tableId/records/:recordId/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-file.md) for the provider-specific parameters and requirements.

