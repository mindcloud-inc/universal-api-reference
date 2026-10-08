# Fleetworthy: Get Person File Info



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person-file-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person-file-info?connectionId=$CONNECTION_ID&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person-file-info?${params}`, {
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
| `personId` | string | yes | The Fleetworthy person UUID. |
| `onlyActiveDocuments` | boolean | no | Limit file information to active company and regulated documents. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "regulatedDocumentCpFileInfos": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `regulatedDocumentCpFileInfos` | array<object> | Regulated documents and their associated Fleetworthy files. |

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /people/file-info` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-file-info.md) for the provider-specific parameters and requirements.

