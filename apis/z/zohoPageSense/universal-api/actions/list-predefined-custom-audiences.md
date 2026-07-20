# Zoho PageSense: List Predefined & Custom Audiences

Retrieves predefined and custom audiences from Zoho PageSense.

```
GET https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-predefined-custom-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-predefined-custom-audiences?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&experimentLinkName=https%3A%2F%2Fexample.com&projectLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "experimentLinkName": "https://example.com",
  "projectLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/list-predefined-custom-audiences?${params}`, {
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
| `projectLinkName` | string | yes | Project link name query parameter. |

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
          "audienceIsPreset": true,
          "audienceIsSelected": true,
          "audienceLinkname": "https://example.com",
          "displayName": "Ava Chen",
          "experimentInvolved": 1,
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
| `audiences[].audienceConditionJson` | object | Audience condition definition. |
| `audiences[].audienceDescription` | string | Audience description. |
| `audiences[].audienceId` | string | Audience identifier. |
| `audiences[].audienceIsPreset` | boolean | Whether the audience is predefined. |
| `audiences[].audienceIsSelected` | boolean | Whether the audience is selected for the experiment. |
| `audiences[].audienceLinkname` | string | Machine-safe audience slug. |
| `audiences[].displayName` | string | Audience display name. |
| `audiences[].experimentInvolved` | number | Experiment usage count when present. |
| `audiences[].success` | boolean | Whether the audience entry was processed successfully. |
| `count` | number | Number of audiences returned. |
| `statusCode` | string | Zoho API status code. |
| `statusString` | string | Human-readable status message. |
| `timeTakenToProcessTheRequest` | string | Server processing time. |

## Native endpoint

Through the native Zoho PageSense API, this operation is `GET https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/audiences` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-predefined-custom-audiences.md) for the provider-specific parameters and requirements.

