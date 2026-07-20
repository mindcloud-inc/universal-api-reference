# Quantcast: Get Async Attributed Actions Report Download URL

Retrieves an async attributed actions report download URL from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-async-attributed-actions-report-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-async-attributed-actions-report-download-url?connectionId=$CONNECTION_ID&entity=%7Btype%3AACCOUNT%2Cid%3A9974296%7D&reportRequestId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity": "{type:ACCOUNT,id:9974296}",
  "reportRequestId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-async-attributed-actions-report-download-url?${params}`, {
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
| `entity` | string | yes | GraphQL EntityInput literal, for example {type: ACCOUNT, id: 123}. Default: `{type:ACCOUNT,id:9974296}`. |
| `reportRequestId` | number | yes | Async report request ID returned by Quantcast. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asyncAttributedActionsReportDownloadURL": {
        "downloadUrl": "https://example.com",
        "reportRequestId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asyncAttributedActionsReportDownloadURL` | object | Download information for an async attributed actions report. |
| `asyncAttributedActionsReportDownloadURL.downloadUrl` | string | Signed download URL for the generated report. |
| `asyncAttributedActionsReportDownloadURL.reportRequestId` | number | Async attributed actions report identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-attributed-actions-report-download-url.md) for the provider-specific parameters and requirements.

