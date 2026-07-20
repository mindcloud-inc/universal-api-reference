# Sumsub: List Verification Levels



```
GET https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-verification-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-verification-levels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-verification-levels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "applicantType": "string",
      "autoCheckGeneratorSettings": {
        "autoCheckMode": "string"
      },
      "clientId": "string",
      "created": {
        "clientSubject": "string",
        "date": "string"
      },
      "createdAt": "string",
      "createdBy": "string",
      "crossCheckPresetId": "string",
      "desc": "string",
      "id": "string",
      "modified": {
        "clientSubject": "string",
        "date": "string"
      },
      "modifiedAt": "string",
      "name": "Ava Chen",
      "requiredIdDocs": {
        "docSets": [
          {
            "idDocSetType": "string",
            "videoRequired": "string"
          }
        ]
      },
      "type": "string",
      "websdkNext": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantType` | string |  |
| `autoCheckGeneratorSettings.autoCheckMode` | string |  |
| `clientId` | string |  |
| `created.clientSubject` | string |  |
| `created.date` | string |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `crossCheckPresetId` | string |  |
| `desc` | string |  |
| `id` | string |  |
| `modified.clientSubject` | string |  |
| `modified.date` | string |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `requiredIdDocs.docSets[].idDocSetType` | string |  |
| `requiredIdDocs.docSets[].videoRequired` | string |  |
| `type` | string |  |
| `websdkNext` | boolean |  |

## Native endpoint

Through the native Sumsub API, this operation is `GET /resources/applicants/-/levels` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-verification-levels.md) for the provider-specific parameters and requirements.

