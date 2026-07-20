# Zoho PageSense: List Selected Audiences

Retrieves selected audiences from Zoho PageSense.

```
GET https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-selected-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-selected-audiences?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&experimentLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "experimentLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-selected-audiences?${params}`, {
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
| `portalName` | string | yes | Portal identifier in the path. |
| `experimentLinkName` | string | yes | Experiment link name query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audiences": [
        {
          "audienceConditionJson": {},
          "audienceDescription": "string",
          "audienceId": "string",
          "audienceIsSelected": true,
          "audienceLinkname": "https://example.com",
          "displayName": "Ava Chen",
          "success": true
        }
      ],
      "count": 1,
      "statusCode": "string",
      "statusString": "string",
      "timeTakenToProcessTheRequest": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audiences[].audienceConditionJson` | object |  |
| `audiences[].audienceDescription` | string |  |
| `audiences[].audienceId` | string |  |
| `audiences[].audienceIsSelected` | boolean |  |
| `audiences[].audienceLinkname` | string |  |
| `audiences[].displayName` | string |  |
| `audiences[].success` | boolean |  |
| `count` | number |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `GET https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/audiences` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-selected-audiences.md) for the provider-specific parameters and requirements.

