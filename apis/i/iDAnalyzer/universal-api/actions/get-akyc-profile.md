# ID Analyzer: Get a KYC profile

Retrieves a KYC profile from ID Analyzer.

```
GET https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/get-akyc-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ID Analyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/get-akyc-profile?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/get-akyc-profile?${params}`, {
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
| `profileId` | string | yes | KYC profile ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ID Analyzer API returns.

## Native endpoint

Through the native ID Analyzer API, this operation is `GET /profile/:profileId` (base URL `https://api2.idanalyzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-akyc-profile.md) for the provider-specific parameters and requirements.

